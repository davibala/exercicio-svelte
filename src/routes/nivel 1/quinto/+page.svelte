<script lang="ts">

    // Implementar uma página que, dados um array bidimensional e um número, subtrai o número de todos os elementos do array;

    let arr:number[][] = [[1,2,3],[4,5,6],[7,8,9]]
    let n:number = 1
    let resultarr:number[][] = [[],[],[]]

    for(let i:number = 0;i<arr.length;i++){
        for(let j:number = 0;j<arr[i].length;j++){
            resultarr[i][j] = arr[i][j] - n
        }
    }

</script>

<div class="container">
    <div class="n1-q5">
        <h2>
            5 - Implementar uma página que, dados um array bidimensional e um número, subtrai o número de todos os elementos do array.
        </h2>
        <div id="idn1q5">
            <h3>Nosso número : {n}</h3>
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
                {#each resultarr as linha}
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


