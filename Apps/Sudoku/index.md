<!DOCTYPE html>
<html lang="ja">
<head>
<!-- 
  ナンプレアプリ (Sudoku App)
  Version: 1.2.0 (Logic Engine + PWA Fix)
  Target: Senior / High-Performance
  Last Updated: 2025-12-27
-->
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="theme-color" content="#F5F5DC">

<!-- PWA Icons & Manifest (Data URI) -->
<link rel="icon" type="image/svg+xml" href="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA1MTIgNTEyIj48cmVjdCB3aWR0aD0iNTEyIiBoZWlnaHQ9IjUxMiIgZmlsbD0iI0Y1RjVEQyIvPjx0ZXh0IHg9IjUwJSIgeT0iNTAlIiBkb21pbmFudC1iYXNlbGluZT0ibWlkZGxlIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIiBmb250LXNpemU9IjMwMCIgZmlsbD0iIzAwMDAzMyIgZm9udC1mYW1pbHk9InNhbnMtc2VyaWYiIGZvbnQtd2VpZ2h0PSJib2xkIj45PC90ZXh0Pjwvc3ZnPg==">
<link rel="apple-touch-icon" href="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA1MTIgNTEyIj48cmVjdCB3aWR0aD0iNTEyIiBoZWlnaHQ9IjUxMiIgZmlsbD0iI0Y1RjVEQyIvPjx0ZXh0IHg9IjUwJSIgeT0iNTAlIiBkb21pbmFudC1iYXNlbGluZT0ibWlkZGxlIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIiBmb250LXNpemU9IjMwMCIgZmlsbD0iIzAwMDAzMyIgZm9udC1mYW1pbHk9InNhbnMtc2VyaWYiIGZvbnQtd2VpZ2h0PSJib2xkIj45PC90ZXh0Pjwvc3ZnPg==">
<link rel="manifest" href='data:application/manifest+json;base64,ewogICJuYW1lIjogIuODcheODs+ODl+ODrCIsCiAgInNob3J0X25hbWUiOiAi44Oy44Oz44OX44Gldmlld190eXBlIjogInN0YW5kYWxvbmUiLAogICJkaXNwbGF5IjogInN0YW5kYWxvbmUiLAogICJiYWNrZ3JvdW5kX2NvbG9yIjogIiNGNUY1REMiLAogICJ0aGVtZV9jb2xvciI6ICIjRjVGNURDIiwKICAiaWNvbnMiOiBbCiAgICB7CiAgICAgICJzcmMiOiAiZGF0YTppbWFnZS9zdmcreG1sO2Jhc2U2NCxQSE4yWnlCM2IzVjBkMzE5Y3ovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA1MTIgNTEyIj48cmVjdCB3aWR0aD0iNTEyIiBoZWlnaHQ9IjUxMiIgZmlsbD0iI0Y1RjVEQyIvPjx0ZXh0IHg9IjUwJSIgeT0iNTAlIiBkb21pbmFudC1iYXNlbGluZT0ibWlkZGxlIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIiBmb250LXNpemU9IjMwMCIgZmlsbD0iIzAwMDAzMyIgZm9udC1mYW1pbHk9InNhbnMtc2VyaWYiIGZvbnQtd2VpZ2h0PSJib2xkIj45PC90ZXh0Pjwvc3ZnPg0iLAogICAgICAic2l6ZXMiOiAiMTkyeDE5MiIsCiAgICAgICJ0eXBlIjogImltYWdlL3N2Zyt4bWwiCiAgICB9CiAgXQp9'>

<title>ナンプレ</title>

<style>
  /* =========================================
     1. DESIGN SYSTEM & RESET
     ========================================= */
  :root {
    --bg-color: #F5F5DC;       /* 背景：アイボリー */
    --text-color: #000033;     /* 文字：濃紺 */
    --grid-line: #555555;      /* 枠線：濃いグレー */
    --cell-bg: #FDFDF0;        /* マス背景：明るいアイボリー */
    --select-bg: #FFFFA0;      /* 選択中：淡い黄色 */
    --highlight-cross: #EBEBE0;/* 十字ハイライト：極薄グレー */
    --btn-bg: #E0E0D0;         /* ボタン背景 */
    --btn-text: #000000;       /* ボタン文字 */
    --memo-color: #555555;     /* メモ文字 */
    --memo-mode-bg: #D0D0D0;   /* メモモードON時 */
    --error-color: #D00000;    /* エラー：赤 */
    --fixed-color: #000033;    /* 初期配置数字 */
    --input-color: #0055AA;    /* 入力数字（青み） */
    --gold-color: #DAA520;     /* 完成時の金色 */
  }

  * {
    box-sizing: border-box;
    -webkit-tap-highlight-color: transparent;
    touch-action: manipulation;
    user-select: none;
    -webkit-touch-callout: none;
  }

  body {
    background-color: var(--bg-color);
    color: var(--text-color);
    font-family: "Hiragino Sans", "Hiragino Kaku Gothic ProN", "Noto Sans JP", sans-serif;
    font-weight: bold;
    margin: 0;
    padding: 0;
    width: 100%;
    height: 100dvh;
    display: flex;
    flex-direction: column;
    overflow: hidden;
  }

  /* =========================================
     2. BASE LAYOUT (縦画面デフォルト)
     ========================================= */
  header {
    grid-area: header;
    width: 100%;
    padding: 8px 15px;
    background-color: var(--bg-color);
    border-bottom: 2px solid var(--grid-line);
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 50px;
    flex-shrink: 0;
    z-index: 10;
  }
  header h1 { font-size: 1.2rem; margin: 0; flex: 1; text-align: center; }
  .header-btn { font-size: 0.9rem; padding: 5px 10px; height: 36px; min-width: auto; }

  /* メインコンテナ */
  #game-container {
    flex: 1;
    width: 100%;
    padding: 10px;
    display: grid;
    gap: 10px;
    overflow-y: auto;
    
    /* 縦画面：サンドイッチ配置 */
    grid-template-columns: 1fr;
    grid-template-rows: auto 1fr auto;
    grid-template-areas:
      "funcs"
      "board"
      "numpad";
    justify-items: center;
  }

  /* エリア定義 */
  #func-buttons { grid-area: funcs; width: 100%; max-width: 500px; }
  #sudoku-board { grid-area: board; }
  #numpad       { grid-area: numpad; width: 100%; max-width: 500px; }

  /* 横画面専用ボタン (初期は非表示) */
  .landscape-only { display: none !important; }

  /* =========================================
     3. BOARD STYLES (盤面)
     ========================================= */
  #sudoku-board {
    display: grid;
    grid-template-columns: repeat(9, minmax(0, 1fr));
    grid-template-rows: repeat(9, minmax(0, 1fr));
    width: min(96vw, 55vh); 
    aspect-ratio: 1 / 1;
    min-height: 0;
    min-width: 0;
    justify-self: center;
    align-self: center;

    border: 3px solid var(--grid-line);
    background-color: var(--grid-line);
    gap: 1px;
    transition: border-color 1.5s ease, box-shadow 1.5s ease;
  }
  
  #sudoku-board.completed {
    border-color: var(--gold-color);
    box-shadow: 0 0 20px var(--gold-color);
  }

  .cell {
    background-color: var(--cell-bg);
    position: relative;
    width: 100%; height: 100%;
    cursor: pointer;
    overflow: hidden;
  }

  .cell-content {
    position: absolute; top: 0; left: 0; width: 100%; height: 100%;
    display: flex; align-items: center; justify-content: center;
    font-size: clamp(1.2rem, 5vw, 2.2rem);
    font-variant-numeric: tabular-nums; 
    z-index: 2;
  }

  /* 3x3ブロック境界線 */
  .cell:nth-child(3n):not(:nth-child(9n))::after {
    content: ''; position: absolute; top: 0; right: -2px; width: 3px; height: 100%;
    background-color: var(--grid-line); z-index: 5; pointer-events: none;
  }
  .cell:nth-child(n+19):nth-child(-n+27)::before,
  .cell:nth-child(n+46):nth-child(-n+54)::before {
    content: ''; position: absolute; bottom: -2px; left: 0; width: 100%; height: 3px;
    background-color: var(--grid-line); z-index: 5; pointer-events: none;
  }

  /* ハイライト関係 */
  .cell.selected { background-color: var(--select-bg); z-index: 3; }
  /* 十字ハイライト */
  .cell.highlight-cross { background-color: var(--highlight-cross); }
  
  /* 文字色制御 */
  .cell.fixed .cell-content { color: var(--fixed-color); }
  .cell.user-input .cell-content { color: var(--input-color); }
  
  /* エラー (即時判定) */
  .cell.error-text .cell-content { color: var(--error-color); }
  
  @keyframes shake { 0%, 100% { transform: translateX(0); } 25% { transform: translateX(-4px); } 75% { transform: translateX(4px); } }
  .cell.shake { animation: shake 0.3s ease-in-out; }

  .memo-grid {
    display: grid; grid-template-columns: repeat(3, 1fr); width: 100%; height: 100%; padding: 1px;
  }
  .memo-grid span { 
    display: flex; align-items: center; justify-content: center;
    font-size: clamp(8px, 1.8vw, 12px); color: var(--memo-color); line-height: 1;
  }

  /* =========================================
     4. BUTTONS
     ========================================= */
  button {
    background-color: var(--btn-bg);
    border: 2px solid #999;
    border-radius: 8px;
    padding: 4px;
    font-size: 1rem;
    font-weight: bold;
    color: var(--btn-text);
    -webkit-text-fill-color: var(--btn-text);
    cursor: pointer;
    transition: transform 0.05s ease;
    white-space: nowrap;
  }
  button:active { transform: scale(0.96); background-color: #CCC; }
  button span.icon { font-size: 1.4rem; margin-right: 2px; }

  #func-buttons { display: flex; justify-content: space-between; gap: 5px; }
  .func-btn {
    flex: 1;
    min-height: 50px;
    display: flex; flex-direction: column; align-items: center; justify-content: center;
    line-height: 1.1;
  }
  .func-btn span.icon { margin: 0 0 2px 0; font-size: 1.6rem; }

  #numpad { 
    display: grid; grid-template-columns: repeat(5, 1fr); gap: 6px; 
  }
  .num-btn { 
    min-height: 50px; aspect-ratio: 1.2;
    font-size: 2rem; 
    font-family: inherit; font-variant-numeric: tabular-nums;
    padding: 0;
    display: flex; align-items: center; justify-content: center;
  }
  .btn-clear {
    min-height: 50px; font-size: 0.9rem !important;
    display: flex; flex-direction: column; align-items: center; justify-content: center;
    gap: 0; line-height: 1.1; background-color: #E8E8E8;
  }
  .btn-clear .icon { font-size: 1.5rem; margin: 0; }

  body.memo-mode .num-btn { background-color: var(--memo-mode-bg); border-color: #666; }
  #btn-memo.active { background-color: var(--memo-mode-bg); border: 3px solid #333; }
  .num-btn.active-match { background-color: var(--select-bg); border-color: var(--text-color); border-width: 3px; }

  /* =========================================
     5. MODAL & TOAST
     ========================================= */
  #overlay {
    display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    background: rgba(245, 245, 220, 0.85); z-index: 100;
    flex-direction: column; align-items: center; justify-content: center; text-align: center;
    animation: fadeIn 0.2s ease;
  }
  @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
  #overlay-content {
    background: #FFF; border: 4px solid var(--text-color); padding: 30px; border-radius: 16px;
    width: 90%; max-width: 450px; display: flex; flex-direction: column; gap: 20px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.15);
  }
  #overlay-msg { font-size: 1.4rem; white-space: pre-wrap; line-height: 1.6; }
  .dialog-btns { display: flex; flex-direction: column; gap: 10px; width: 100%; }
  .dialog-btns button { width: 100%; font-size: 1.2rem; padding: 15px; }

  #toast {
    position: fixed; bottom: 30px; left: 50%; transform: translateX(-50%);
    background-color: var(--text-color); color: #FFF; padding: 12px 24px;
    border-radius: 50px; font-size: 1rem; opacity: 0; pointer-events: none;
    transition: opacity 0.3s; z-index: 200;
  }
  #toast.show { opacity: 0.95; }

  /* =========================================
     6. MEDIA QUERY (横画面最適化)
     ========================================= */
  @media (min-aspect-ratio: 1.1/1) {
    header { display: none; } /* 横画面ではヘッダー非表示 */
    
    #game-container {
      /* 右側の操作パネルをスリム化 */
      grid-template-columns: auto 240px;
      grid-template-rows: auto 1fr;
      grid-template-areas:
        "board funcs"
        "board numpad";
      
      /* 上切れ防止: スクロール可能に */
      align-content: start; 
      justify-content: center;
      gap: 15px;
      padding: 10px 20px;
      overflow-y: auto;
    }

    #sudoku-board {
      width: auto;
      height: min(94vh, 94vw);
      aspect-ratio: 1 / 1;
      margin-bottom: 20px;
    }

    /* 横画面用のボタンを表示 */
    .landscape-only { display: flex !important; }

    #func-buttons {
      display: grid !important;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
      align-self: end;
      margin-bottom: 10px;
    }
    
    #numpad {
      grid-template-columns: repeat(3, 1fr);
      align-self: start;
    }
    
    .btn-clear { grid-column: 1 / -1; aspect-ratio: auto; min-height: 55px; }
    .num-btn, #func-buttons button { aspect-ratio: auto; flex: 1; min-height: 0; }
  }
</style>
</head>
<body>

<header>
  <button id="btn-help" class="header-btn">❓使い方</button>
  <h1 id="title-label">ナンプレ</h1>
  <button id="btn-new" class="header-btn">🆕新規</button>
</header>

<div id="game-container">
  <div id="func-buttons">
    <!-- 横画面用ボタン -->
    <button id="btn-ls-help" class="func-btn landscape-only"><span class="icon">❓</span>使い方</button>
    <button id="btn-ls-new" class="func-btn landscape-only"><span class="icon">🆕</span>新規</button>
    
    <!-- 通常機能ボタン -->
    <button id="btn-undo" class="func-btn"><span class="icon">↩️</span>もどる</button>
    <button id="btn-check" class="func-btn"><span class="icon">✅</span>判定</button>
    <button id="btn-memo" class="func-btn"><span class="icon">✏️</span>メモ</button>
    <button id="btn-hint" class="func-btn"><span class="icon">💡</span>ヒント</button>
  </div>

  <div id="sudoku-board"></div>
  <div id="numpad"></div>
</div>

<div id="overlay">
  <div id="overlay-content">
    <div id="overlay-msg"></div>
    <div class="dialog-btns" id="dialog-actions"></div>
  </div>
</div>
<div id="toast"></div>

<script>
/**
 * [CONFIG] 設定値
 */
const CONFIG = {
  VERSION: '1.2.0',
  DIFFICULTY: {
    EASY:   { count: 36, label: "⭐ かんたん", logic: 'basic' },
    NORMAL: { count: 46, label: "⭐⭐ ふつう", logic: 'normal' },
    HARD:   { count: 54, label: "⭐⭐⭐ むずかしい", logic: 'hard' },
    MASTER: { count: 62, label: "👑 達人", logic: 'hard' }
  },
  TIMEOUT_MS: 2000 
};

/**
 * [ENGINE] 高速演算 + 人間思考ロジック
 */
const Engine = {
  ROWS: new Int16Array(9), COLS: new Int16Array(9), BOXES: new Int16Array(9),
  
  reset() { this.ROWS.fill(0); this.COLS.fill(0); this.BOXES.fill(0); },
  
  toggle(r, c, num) {
    const bit = 1 << (num - 1);
    this.ROWS[r] ^= bit; this.COLS[c] ^= bit;
    this.BOXES[Math.floor(r/3)*3 + Math.floor(c/3)] ^= bit;
  },
  
  isValid(r, c, num) {
    const bit = 1 << (num - 1);
    const boxIdx = Math.floor(r/3)*3 + Math.floor(c/3);
    return !((this.ROWS[r] & bit) | (this.COLS[c] & bit) | (this.BOXES[boxIdx] & bit));
  },
  
  setBoard(board) {
    this.reset();
    for(let r=0; r<9; r++) for(let c=0; c<9; c++) 
      if(board[r][c] !== 0) this.toggle(r, c, board[r][c]);
  },
  
  // Backtracking Solver (for verification and generation)
  solve(board, countOnly = false, limit = 2) {
    let bestR = -1, bestC = -1, minOptions = 10;
    for(let r=0; r<9; r++){
      for(let c=0; c<9; c++){
        if(board[r][c] === 0) {
          let options = 0;
          const used = this.ROWS[r] | this.COLS[c] | this.BOXES[Math.floor(r/3)*3 + Math.floor(c/3)];
          for(let n=1; n<=9; n++) if(!((used >> (n-1)) & 1)) options++;
          if(options < minOptions) { minOptions = options; bestR = r; bestC = c; if(minOptions <= 1) break; }
        }
      }
      if(minOptions <= 1) break;
    }
    if(bestR === -1) return 1;

    let count = 0;
    const r = bestR, c = bestC;
    for(let num=1; num<=9; num++){
      if(this.isValid(r, c, num)) {
        board[r][c] = num; this.toggle(r, c, num);
        if(countOnly) {
          count += this.solve(board, true, limit - count);
          if(count >= limit) { this.toggle(r, c, num); board[r][c] = 0; return count; }
        } else {
          if(this.solve(board)) return true;
        }
        this.toggle(r, c, num); board[r][c] = 0;
      }
    }
    return countOnly ? count : false;
  },

  // Human Logic Simulator (for Difficulty Check)
  canSolveLogically(boardStart, level) {
    // level: 'basic' (Naked Single only), 'normal' (Hidden Single allowed)
    let board = JSON.parse(JSON.stringify(boardStart));
    let progress = true;
    let filled = 0;
    const initialEmpty = board.flat().filter(x=>x===0).length;

    while(progress) {
      progress = false;
      let candidates = [];
      
      // 1. Calculate candidates for all cells
      for(let r=0; r<9; r++) {
        candidates[r] = [];
        for(let c=0; c<9; c++) {
          if(board[r][c] !== 0) { candidates[r][c] = null; continue; }
          let opts = [];
          for(let n=1; n<=9; n++) {
            // Simplified check: Check local row/col/box in current board state
            // (Note: For rigorous check, we need bitmask updates, but simple iteration is enough for logic sim)
            if(this.checkSafe(board, r, c, n)) opts.push(n);
          }
          candidates[r][c] = opts;
        }
      }

      // 2. Strategy: Naked Single
      for(let r=0; r<9; r++) {
        for(let c=0; c<9; c++) {
          if(board[r][c]===0 && candidates[r][c].length === 1) {
            board[r][c] = candidates[r][c][0];
            filled++;
            progress = true;
          }
        }
      }
      if(progress) continue;

      // 3. Strategy: Hidden Single (Only for Normal+)
      if(level !== 'basic') {
        if(this.applyHiddenSingle(board, candidates)) {
          progress = true;
          filled++;
        }
      }
    }
    
    // Check if fully solved
    return board.flat().every(x => x !== 0);
  },

  checkSafe(board, r, c, num) {
    for(let i=0; i<9; i++) if(board[r][i]===num || board[i][c]===num) return false;
    const sr=Math.floor(r/3)*3, sc=Math.floor(c/3)*3;
    for(let i=0; i<3; i++) for(let j=0; j<3; j++) if(board[sr+i][sc+j]===num) return false;
    return true;
  },

  applyHiddenSingle(board, candidates) {
    // Check Rows, Cols, Boxes for a number that appears in only one candidate slot
    const checkUnit = (cells) => {
      let counts = Array(10).fill(0);
      let pos = Array(10).fill(null);
      for(let {r,c} of cells) {
        if(board[r][c] !== 0) continue;
        const opts = candidates[r][c];
        if(!opts) continue;
        opts.forEach(n => { counts[n]++; pos[n] = {r,c}; });
      }
      for(let n=1; n<=9; n++) {
        if(counts[n] === 1) {
          const {r,c} = pos[n];
          board[r][c] = n;
          return true; // Applied one
        }
      }
      return false;
    };

    // Rows
    for(let r=0; r<9; r++) {
      let cells = []; for(let c=0; c<9; c++) cells.push({r,c});
      if(checkUnit(cells)) return true;
    }
    // Cols
    for(let c=0; c<9; c++) {
      let cells = []; for(let r=0; r<9; r++) cells.push({r,c});
      if(checkUnit(cells)) return true;
    }
    // Boxes
    for(let br=0; br<3; br++) for(let bc=0; bc<3; bc++) {
      let cells = [];
      for(let i=0; i<3; i++) for(let j=0; j<3; j++) cells.push({r:br*3+i, c:bc*3+j});
      if(checkUnit(cells)) return true;
    }
    return false;
  }
};

/**
 * [STORAGE]
 */
const Storage = {
  KEY: 'seniorSudokuApp_v3',
  save(state) {
    try {
      const { history, isGenerating, ...data } = state; 
      localStorage.setItem(this.KEY, JSON.stringify(data));
    } catch(e) {}
  },
  load() {
    try {
      const data = localStorage.getItem(this.KEY);
      return data ? JSON.parse(data) : null;
    } catch(e) { return null; }
  },
  checkBirthday() {
    const today = new Date();
    if (today.getMonth() === 1 && today.getDate() === 20) {
      const key = 'bday_' + today.getFullYear();
      if (!localStorage.getItem(key)) {
        setTimeout(() => {
          UI.showDialog("🎉 お誕生日おめでとうございます！ 🎉\n\n素敵な1年になりますように。", [{text: "ありがとう", action: UI.closeDialog}]);
          localStorage.setItem(key, 'true');
        }, 1000);
      }
    }
  }
};

/**
 * [UI] 表示・描画
 */
const UI = {
  dom: {},
  toastTimer: null,

  init() {
    this.dom = {
      board: document.getElementById('sudoku-board'),
      numpad: document.getElementById('numpad'),
      btnMemo: document.getElementById('btn-memo'),
      overlay: document.getElementById('overlay'),
      title: document.getElementById('title-label'),
      toast: document.getElementById('toast')
    };
    this.createNumpad();
  },

  createNumpad() {
    this.dom.numpad.innerHTML = '';
    for (let i = 1; i <= 9; i++) {
      const btn = document.createElement('button');
      btn.className = 'num-btn';
      btn.id = `btn-num-${i}`;
      btn.textContent = i;
      btn.onclick = () => App.handleInput(i);
      this.dom.numpad.appendChild(btn);
    }
    const btnClear = document.createElement('button');
    btnClear.className = 'btn-clear';
    btnClear.innerHTML = `<span class="icon">🧹</span><span class="label">消去</span>`;
    btnClear.onclick = () => App.handleInput(0);
    this.dom.numpad.appendChild(btnClear);
  },

  renderBoard(puzzle, fixed, selected, memos, solution, completed) {
    const board = this.dom.board;
    board.innerHTML = '';
    board.classList.toggle('completed', completed);

    const selR = selected ? selected.r : -1;
    const selC = selected ? selected.c : -1;

    for (let r = 0; r < 9; r++) {
      for (let c = 0; c < 9; c++) {
        const val = puzzle[r][c];
        const isFixed = fixed[r][c];
        const cell = document.createElement('div');
        cell.className = 'cell';
        cell.dataset.r = r; cell.dataset.c = c;

        if (isFixed) cell.classList.add('fixed');
        else if (val !== 0) cell.classList.add('user-input');
        
        if (selected && selected.r === r && selected.c === c) {
          cell.classList.add('selected');
        } else if (selected && (r === selR || c === selC)) {
          // Cross highlight (Row & Col)
          cell.classList.add('highlight-cross');
        }

        // Real-time error (Immediate feedback)
        if (!isFixed && val !== 0 && val !== solution[r][c]) {
          cell.classList.add('error-text');
        }

        const content = document.createElement('div');
        content.className = 'cell-content';
        if (val !== 0) content.textContent = val;
        else this.renderMemos(content, memos[r][c]);

        cell.appendChild(content);
        cell.onclick = () => App.selectCell(r, c, isFixed);
        board.appendChild(cell);
      }
    }
    this.updateNumpad(selected ? puzzle[selected.r][selected.c] : 0);
  },

  renderMemos(container, list) {
    const div = document.createElement('div');
    div.className = 'memo-grid';
    const safeList = list || [];
    for (let m = 1; m <= 9; m++) {
      const span = document.createElement('span');
      span.textContent = safeList.includes(m) ? m : '';
      div.appendChild(span);
    }
    container.appendChild(div);
  },

  updateNumpad(val) {
    document.querySelectorAll('.num-btn').forEach(b => b.classList.remove('active-match'));
    if (val >= 1 && val <= 9) {
      document.getElementById(`btn-num-${val}`)?.classList.add('active-match');
    }
  },

  updateTitle(label) { this.dom.title.textContent = `ナンプレ (${label})`; },
  
  toggleMemoMode(isMemo) {
    document.body.classList.toggle('memo-mode', isMemo);
    this.dom.btnMemo.classList.toggle('active', isMemo);
  },

  shakeCell(r, c) {
    const cell = document.querySelector(`.cell[data-r="${r}"][data-c="${c}"]`);
    if(cell) {
      cell.classList.remove('shake');
      void cell.offsetWidth;
      cell.classList.add('shake');
    }
  },

  showDialog(msg, buttons) {
    document.getElementById('overlay-msg').textContent = msg;
    const actions = document.getElementById('dialog-actions');
    actions.innerHTML = '';
    buttons.forEach(conf => {
      const btn = document.createElement('button');
      btn.textContent = conf.text;
      btn.onclick = conf.action;
      actions.appendChild(btn);
    });
    this.dom.overlay.style.display = 'flex';
  },
  closeDialog() { document.getElementById('overlay').style.display = 'none'; },

  showToast(msg) {
    if (this.toastTimer) clearTimeout(this.toastTimer);
    const toast = this.dom.toast;
    toast.textContent = msg;
    toast.classList.add('show');
    this.toastTimer = setTimeout(() => toast.classList.remove('show'), 3000);
  }
};

/**
 * [APP] メインロジック
 */
const App = {
  state: {
    solution: [], puzzle: [], fixed: [], memos: [], history: [],
    selectedCell: null, isMemoMode: false, isComplete: false,
    diffKey: 'NORMAL', isGenerating: false
  },

  init() {
    UI.init();
    this.bindEvents();
    Storage.checkBirthday();
    window.addEventListener('contextmenu', e => e.preventDefault());

    const saved = Storage.load();
    if (saved && saved.puzzle) {
      this.state = { ...this.state, ...saved, history: [], isGenerating: false };
      this.refresh();
      const label = CONFIG.DIFFICULTY[this.state.diffKey] ? CONFIG.DIFFICULTY[this.state.diffKey].label : "ふつう";
      UI.updateTitle(label);
      if (!this.state.isComplete) UI.showToast("続きから始めます");
    } else {
      this.startNewGame('NORMAL');
    }
  },

  bindEvents() {
    const guard = (fn) => { if(!this.state.isGenerating) fn(); };
    const bindBtn = (id, action) => { const el = document.getElementById(id); if(el) el.onclick = () => guard(action); };

    bindBtn('btn-help', () => this.showHelp());
    bindBtn('btn-new',  () => this.promptNewGame());
    bindBtn('btn-ls-help', () => this.showHelp()); // Landscape
    bindBtn('btn-ls-new',  () => this.promptNewGame()); // Landscape

    bindBtn('btn-undo',  () => this.undo());
    bindBtn('btn-check', () => this.checkErrors());
    bindBtn('btn-memo',  () => this.toggleMemo());
    bindBtn('btn-hint',  () => this.giveHint());
    
    window.addEventListener('keydown', e => {
      if (this.state.isGenerating || document.getElementById('overlay').style.display === 'flex') return;
      if ((e.ctrlKey || e.metaKey) && e.key === 'z') { e.preventDefault(); this.undo(); return; }
      if (e.key.startsWith('Arrow')) { e.preventDefault(); this.moveSelection(e.key); return; }
      if (e.key >= '1' && e.key <= '9') { this.handleInput(parseInt(e.key)); return; }
      if (['Backspace','Delete','0'].includes(e.key)) { this.handleInput(0); return; }
    });
  },

  refresh() {
    UI.renderBoard(
      this.state.puzzle, this.state.fixed, this.state.selectedCell,
      this.state.memos, this.state.solution, this.state.isComplete
    );
    UI.toggleMemoMode(this.state.isMemoMode);
  },

  save() { Storage.save(this.state); },
  saveHistory() {
    if(this.state.history.length > 20) this.state.history.shift();
    this.state.history.push({
      puzzle: JSON.stringify(this.state.puzzle),
      memos: JSON.stringify(this.state.memos)
    });
  },

  selectCell(r, c, isFixed) {
    if(this.state.isGenerating) return;
    if (isFixed) UI.shakeCell(r, c);
    this.state.selectedCell = { r, c };
    this.refresh();
  },

  moveSelection(key) {
    if (!this.state.selectedCell) { this.selectCell(4, 4, this.state.fixed[4][4]); return; }
    let { r, c } = this.state.selectedCell;
    if (key === 'ArrowUp') r = Math.max(0, r - 1);
    if (key === 'ArrowDown') r = Math.min(8, r + 1);
    if (key === 'ArrowLeft') c = Math.max(0, c - 1);
    if (key === 'ArrowRight') c = Math.min(8, c + 1);
    this.selectCell(r, c, this.state.fixed[r][c]);
  },

  handleInput(num) {
    if (this.state.isComplete || this.state.isGenerating) return;
    if (!this.state.selectedCell) { UI.showDialog("入力するマスを\n選んでください。", [{text:"OK", action:UI.closeDialog}]); return; }
    const { r, c } = this.state.selectedCell;
    if (this.state.fixed[r][c]) { UI.shakeCell(r, c); return; }

    this.saveHistory();

    if (num === 0) {
      this.state.puzzle[r][c] = 0;
      this.state.memos[r][c] = [];
    } else if (this.state.isMemoMode) {
      const list = this.state.memos[r][c];
      const idx = list.indexOf(num);
      if (idx >= 0) list.splice(idx, 1); else { list.push(num); list.sort(); }
    } else {
      this.state.puzzle[r][c] = num;
      for(let i=0; i<9; i++) { this.removeMemo(r, i, num); this.removeMemo(i, c, num); }
      const sr=Math.floor(r/3)*3, sc=Math.floor(c/3)*3;
      for(let i=0; i<3; i++) for(let j=0; j<3; j++) this.removeMemo(sr+i, sc+j, num);
    }
    
    this.refresh();
    if(num !== 0 && !this.state.isMemoMode) this.checkProgress();
    this.save();
  },

  removeMemo(r, c, num) {
    const idx = this.state.memos[r][c].indexOf(num);
    if (idx >= 0) this.state.memos[r][c].splice(idx, 1);
  },

  checkProgress() {
    let full = true, error = false;
    for(let r=0; r<9; r++) for(let c=0; c<9; c++) {
      const val = this.state.puzzle[r][c];
      if(val === 0) full = false;
      else if(val !== this.state.solution[r][c]) error = true;
    }
    if (full && !error) {
      this.state.isComplete = true;
      this.refresh();
      setTimeout(() => UI.showDialog("おめでとうございます！\n見事な完成です。", [{text:"新しい問題へ", action:()=>this.promptNewGame()}]), 600);
    }
  },

  toggleMemo() {
    this.state.isMemoMode = !this.state.isMemoMode;
    this.refresh();
  },

  undo() {
    if (this.state.history.length === 0) return;
    const prev = this.state.history.pop();
    this.state.puzzle = JSON.parse(prev.puzzle);
    this.state.memos = JSON.parse(prev.memos);
    this.state.isComplete = false;
    this.refresh();
    this.save();
  },

  checkErrors() {
    let hasInput = false, found = false;
    for(let r=0; r<9; r++) for(let c=0; c<9; c++) {
      if(!this.state.fixed[r][c] && this.state.puzzle[r][c] !== 0) {
        hasInput = true;
        if(this.state.puzzle[r][c] !== this.state.solution[r][c]) found = true;
      }
    }
    if(!hasInput) {
      UI.showDialog("まだ数字が入力されていません。", [{text:"OK", action:UI.closeDialog}]);
    } else if (found) {
      UI.showDialog("赤い数字のマスが\n間違っています。", [{text:"確認する", action:UI.closeDialog}]);
    } else {
      UI.showToast("現在はすべて正解です！");
    }
  },

  giveHint() {
    if (!this.state.selectedCell) { UI.showDialog("ヒントを使いたいマスを\n選んでください。", [{text:"OK", action:UI.closeDialog}]); return; }
    const {r, c} = this.state.selectedCell;
    if (this.state.fixed[r][c] || this.state.puzzle[r][c] === this.state.solution[r][c]) return;
    this.saveHistory();
    const ans = this.state.solution[r][c];
    this.handleInput(ans);
  },

  promptNewGame() {
    const btns = Object.keys(CONFIG.DIFFICULTY).map(k => ({
      text: CONFIG.DIFFICULTY[k].label,
      action: () => this.startNewGame(k)
    }));
    btns.push({text: "キャンセル", action: UI.closeDialog});
    UI.showDialog("難易度を選んでください", btns);
  },

  startNewGame(diffKey) {
    this.state.isGenerating = true;
    this.state.diffKey = diffKey;
    UI.updateTitle(CONFIG.DIFFICULTY[diffKey].label);
    UI.closeDialog();
    UI.showToast("新しい問題を作成中...");
    
    setTimeout(() => {
      const diff = CONFIG.DIFFICULTY[diffKey];
      this.generate(diff.count, diff.logic);
      
      this.state.history = [];
      this.state.selectedCell = null;
      this.state.isMemoMode = false;
      this.state.isComplete = false;
      this.state.memos = Array.from({length: 9}, () => Array.from({length: 9}, () => []));
      
      this.refresh();
      this.save();
      this.state.isGenerating = false;
      UI.showToast("作成しました！");
    }, 50);
  },

  generate(targetHoles, logicLevel) {
    // 1. Create Base Solution
    const board = Array.from({length:9}, ()=>Array(9).fill(0));
    Engine.setBoard(board);
    for(let i=0; i<9; i+=3) {
      const nums = [1,2,3,4,5,6,7,8,9].sort(()=>Math.random()-0.5);
      for(let r=0; r<3; r++) for(let c=0; c<3; c++) {
        board[i+r][i+c] = nums.pop();
        Engine.toggle(i+r, i+c, board[i+r][i+c]);
      }
    }
    Engine.solve(board);
    this.state.solution = JSON.parse(JSON.stringify(board));
    this.state.puzzle = JSON.parse(JSON.stringify(this.state.solution));
    this.state.fixed = Array.from({length:9}, ()=>Array(9).fill(true));

    // 2. Dig Holes with Logic Check
    let candidates = [];
    for(let r=0; r<9; r++) for(let c=0; c<9; c++) candidates.push({r,c});
    candidates.sort(()=>Math.random()-0.5);

    let holes = 0;
    const start = Date.now();

    for(let cell of candidates) {
      if(Date.now() - start > CONFIG.TIMEOUT_MS) break;
      if(holes >= targetHoles) break;

      const {r, c} = cell;
      if(this.state.puzzle[r][c] === 0) continue;

      const backupVal = this.state.puzzle[r][c];
      
      // Point Symmetry Removal
      const sr = 8-r, sc = 8-c;
      const backupSym = this.state.puzzle[sr][sc];
      
      this.state.puzzle[r][c] = 0;
      this.state.puzzle[sr][sc] = 0;
      
      // Validation Strategy
      let isValid = false;
      
      // Check 1: Unique Solution (Fast)
      Engine.setBoard(this.state.puzzle);
      if(Engine.solve(this.state.puzzle, true, 2) === 1) {
        // Check 2: Logic Quality (If Easy/Normal)
        if (logicLevel !== 'hard') {
          if (Engine.canSolveLogically(this.state.puzzle, logicLevel)) {
            isValid = true;
          }
        } else {
          isValid = true;
        }
      }

      if(isValid) {
        this.state.fixed[r][c] = false;
        this.state.fixed[sr][sc] = false;
        holes += (r===sr && c===sc) ? 1 : 2;
      } else {
        this.state.puzzle[r][c] = backupVal;
        this.state.puzzle[sr][sc] = backupSym;
      }
    }
  },
  
  showHelp() {
    UI.showDialog(
      "【使い方】\n1. マスを選んで数字を入力。\n2. 間違いはすぐに赤字になります。\n\n・[✏️メモ] メモ入力モード\n・[✅判定] 全体の再確認\n・横画面でも快適に遊べます。", 
      [{text: "わかりました", action: UI.closeDialog}]
    );
  }
};

App.init();
</script>
</body>
</html>
