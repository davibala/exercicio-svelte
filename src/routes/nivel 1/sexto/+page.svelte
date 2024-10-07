<script lang="ts">

    // Implementar uma página que, que dado um array bidimensional e um número, divide todos os elementos do array pelo número;

    let arr: number[][] = [[10,20,30],[40,50,60],[70,80,90]];
    let n: number = 10;
    let resultarray: number[][] = [[],[],[]];

    for (let i: number = 0; i < arr.length; i++) {
        for (let j: number = 0; j < arr[i].length; j++) {
            resultarray[i][j] = arr[i][j] / n;
        }
    }
    
</script>

<div class="container">
    <div class="n1-q6">
        <h2>
            6 - Implementar uma página que, que dado um array bidimensional e um número, divide todos os elementos do array pelo número.
        </h2>
        <div id="idn1q6">            
            <h3>Nosso número: {n}</h3>
            <div class="titulo-tabela">
                <h3>Nosso Array :</h3>
                <table class="tabela">
                    {#each arr as linha}
                    <tr>
                        {#each linha as coluna}
                        <td>{coluna}</td>
                        {/each}
                    </tr>
                    {/each}
                </table>
            </div>
        </div>
        <div class="titulo-tabela">
            <h3 class="saida">Saída :</h3>
            <table class="tabela">
                {#each resultarray as linha}
                <tr>
                    {#each linha as coluna}
                    <td>{coluna}</td>
                    {/each}
                </tr>
                {/each}
            </table>
        </div>
    </div>
</div>

<div class="voltar">
    <a class="botao" href="/nivel 1">Voltar</a>
</div>