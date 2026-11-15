# Overlook-Chess-Code
index.html:

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#111714">
  <title>Overlook Chess</title>
  <link rel="stylesheet" href="style.css">
  <script src="script.js" defer></script>
</head>
<body>
  <main class="app">
    <header class="topbar">
      <a class="brand" href="#" aria-label="Overlook Chess home">
        <span class="brand-mark" aria-hidden="true">♞</span>
        <span>OVERLOOK<span class="brand-light"> / CHESS</span></span>
      </a>
      <span class="top-note"><span class="online-dot"></span> LOCAL GAME</span>
    </header>

    <section class="game">
      <div class="board-column">
        <div class="game-heading">
          <div>
            <p class="eyebrow">CLASSIC · TWO PLAYERS</p>
            <h1>The quiet game.</h1>
          </div>
          <span class="game-number">BOARD 01</span>
        </div>

        <div class="board-stage">
          <div class="board-axis" id="board" role="group" aria-label="Chessboard with algebraic coordinates"></div>
        </div>

        <div class="board-caption">
          <span><span class="caption-dot"></span> Coordinates shown on every edge</span>
          <span class="turn-caption" id="turn-caption">WHITE TO MOVE</span>
        </div>
      </div>

      <aside class="sidebar" aria-label="Game controls and information">
        <section class="player-card active-player" id="white-card">
          <div class="player-avatar white-avatar" aria-hidden="true">♔</div>
          <div class="player-info">
            <span class="player-label">WHITE</span>
            <strong id="white-status">Your turn</strong>
          </div>
          <span class="player-dot" aria-hidden="true"></span>
        </section>

        <section class="player-card" id="black-card">
          <div class="player-avatar black-avatar" aria-hidden="true">♚</div>
          <div class="player-info">
            <span class="player-label">BLACK</span>
            <strong id="black-status">Waiting</strong>
          </div>
          <span class="player-dot" aria-hidden="true"></span>
        </section>

        <section class="side-section captured-section">
          <div class="section-heading">
            <h2>Captured pieces</h2>
            <span class="section-note">TAKEN</span>
          </div>
          <div class="captured-row">
            <span class="captured-label">White</span>
            <span class="captured-pieces" id="white-captured" aria-label="Pieces captured by white">—</span>
          </div>
          <div class="captured-row">
            <span class="captured-label">Black</span>
            <span class="captured-pieces" id="black-captured" aria-label="Pieces captured by black">—</span>
          </div>
        </section>

        <section class="side-section moves-section">
          <div class="section-heading">
            <h2>Move history</h2>
            <span class="section-note" id="move-count">00</span>
          </div>
          <ol class="move-list" id="move-list" aria-live="polite">
            <li class="empty-history">Moves will appear here.</li>
          </ol>
        </section>

        <div class="controls">
          <button class="secondary-button" id="undo-button" type="button" disabled>
            <span aria-hidden="true">↶</span> Undo
          </button>
          <button class="secondary-button" id="flip-button" type="button">
            <span aria-hidden="true">⟳</span> Flip board
          </button>
          <button class="new-game-button" id="new-game-button" type="button">
            New game <span aria-hidden="true">↗</span>
          </button>
        </div>

        <p class="help-note">Select a piece, then select a highlighted square to move.</p>
      </aside>
    </section>

    <footer class="footer">
      <span>TAKE YOUR TIME.</span>
      <span>♙ &nbsp; ♟</span>
    </footer>
  </main>

  <dialog class="promotion-dialog" id="promotion-dialog" aria-labelledby="promotion-title">
    <p class="eyebrow">A PAWN HAS REACHED THE END</p>
    <h2 id="promotion-title">Choose a promotion</h2>
    <div class="promotion-choices" id="promotion-choices"></div>
  </dialog>
</body>
</html>
