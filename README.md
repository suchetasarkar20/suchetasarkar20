Hi there 👋, I'm Sucheta Sarkar 
<hr style="border:1px solid #ccc">



## 📊 GitHub Stats
<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=suchetasarkar20&theme=light" alt="GitHub Stats" />
</p>

## Let's play a game. shall we?
<div id="tic-tac-toe" style="text-align: center;">
    <h3>Tic-Tac-Toe</h3>
    <table id="game" border="1" cellpadding="20" style="margin: 0 auto; font-size: 20px;">
        <tr>
            <td onclick="play(0)"></td>
            <td onclick="play(1)"></td>
            <td onclick="play(2)"></td>
        </tr>
        <tr>
            <td onclick="play(3)"></td>
            <td onclick="play(4)"></td>
            <td onclick="play(5)"></td>
        </tr>
        <tr>
            <td onclick="play(6)"></td>
            <td onclick="play(7)"></td>
            <td onclick="play(8)"></td>
        </tr>
    </table>
    <br>
    <button onclick="reset()">Reset</button>
    <p id="message"></p>
</div>

<script>
    var board = ['', '', '', '', '', '', '', '', ''];
    var currentPlayer = 'X';
    var gameActive = true;

    const winningConditions = [
        [0, 1, 2],
        [3, 4, 5],
        [6, 7, 8],
        [0, 3, 6],
        [1, 4, 7],
        [2, 5, 8],
        [0, 4, 8],
        [2, 4, 6]
    ];

    function play(clickedCellIndex) {
        if (board[clickedCellIndex] !== '' || !gameActive) {
            return;
        }

        board[clickedCellIndex] = currentPlayer;
        document.querySelectorAll('td')[clickedCellIndex].innerHTML = currentPlayer;

        let roundWon = false;
        for (let i = 0; i <= 7; i++) {
            const winCondition = winningConditions[i];
            let a = board[winCondition[0]];
            let b = board[winCondition[1]];
            let c = board[winCondition[2]];
            if (a === '' || b === '' || c === '') {
                continue;
            }
            if (a === b && b === c) {
                roundWon = true;
                break;
            }
        }

        if (roundWon) {
            document.getElementById('message').innerHTML = currentPlayer + ' has won!';
            gameActive = false;
            return;
        }

        let roundDraw = !board.includes('');
        if (roundDraw) {
            document.getElementById('message').innerHTML = 'Game ended in a draw!';
            gameActive = false;
            return;
        }

        currentPlayer = currentPlayer === 'X' ? 'O' : 'X';
    }

    function reset() {
        board = ['', '', '', '', '', '', '', '', ''];
        gameActive = true;
        currentPlayer = 'X';
        document.querySelectorAll('td').forEach(cell => cell.innerHTML = '');
        document.getElementById('message').innerHTML = '';
    }
</script>

## 📈 GitHub Activity Graph
<p align="center">
  <img src="https://activity-graph.herokuapp.com/graph?username=suchetasarkar20&bg_color=000000&color=58a6ff&line=58a6ff&point=ffffff&area=true&hide_border=true" alt="GitHub Activity Graph" />
</p>
![suchetasarkar20's Stats](https://github-readme-stats.vercel.app/api?username=suchetasarkar20&theme=default&show_icons=true&hide_border=false&count_private=false)
![suchetasarkar20's Streak](https://github-readme-streak-stats.herokuapp.com/?user=suchetasarkar20&theme=default&hide_border=false)
![suchetasarkar20's Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=suchetasarkar20&theme=default&show_icons=true&hide_border=false&layout=compact)
