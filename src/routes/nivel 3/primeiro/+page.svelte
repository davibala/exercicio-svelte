<script lang="ts">

    import '../../../styles/global.css'
    // Implementar uma página capaz de imprimir as diagonais de array tridimensional.
    // Dica: assuma que o array possui a mesma quantidade de linhas, colunas e páginas


    let arr:number[][][] = [
        [
            [1, 2, 3],
            [4, 5, 6],
            [7, 8, 9]
        ],
        [
            [10, 11, 12],
            [13, 14, 15],
            [16, 17, 18]
        ],
        [
            [19, 20, 21],
            [22, 23, 24],
            [25, 26, 27]
        ]
    ];

    let n:number = arr.length;

    let diagonais:number[][] = []

    for (let i = 0; i < n; i++) {
        diagonais[i] = []
        diagonais[0][i] = arr[i][i][i]
    }

    for (let i = 0; i < n; i++) {
        diagonais[i+1] = []
        diagonais[1][i] = arr[i][i][n - i - 1]
    }

    for (let i = 0; i < n; i++) {
        diagonais[i+2] = []
        diagonais[2][i] = arr[i][n - i - 1][i]
    }

    for (let i = 0; i < n; i++) {
        diagonais[i+3] = []
        diagonais[3][i] = arr[i][n - i - 1][n - i - 1]
    }

</script>

<div class="container">
    <div class="n3-q1">
        <h2>
            1 - Implementar uma página capaz de imprimir as diagonais de array tridimensional.
        </h2>   
        <div id="idn3q1">
            <h3>Elementos do Array:</h3>
            <div class="titulo-tabela">
                {#each arr as page }
                    <table class="tabela">
                        {#each page as linha }
                        <tr>
                            {#each linha as coluna }
                                <td>{coluna}</td>
                            {/each}
                        </tr>
                        {/each}
                    </table><br>
                {/each}
            </div>
        </div>
    
        
        <ul class="respostas">
            <li><h3>Diagonal principal: {diagonais[0]}</h3></li>
            <li><h3>Diagonal secundária: {diagonais[1]}</h3></li>
            <li><h3>Diagonal terciária: {diagonais[2]}</h3></li>
            <li><h3>Diagonal quaternária: {diagonais[3]}</h3></li>
        </ul>
    </div>
</div>


<a class="botao" href="/nivel 3">Voltar</a>