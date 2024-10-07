<script lang="ts">

    // Implementar uma página que, dados dois arrays bidimensionais, escreve no segundo array a transcrição do primeiro;
    // Exemplo: b[linha,coluna] = a[coluna,linha]

    let arr1:number[][] = [[1,2,3],[4,5,6],[7,8,9]]
    let arr2:number[][] = [[0,0,0],[0,0,0],[0,0,0]]
    let arr3:number[][] = [[0,0,0],[0,0,0],[0,0,0]]


    for(let i:number = 0;i<arr1.length;i++){
        for(let j:number = 0;j<arr1[i].length;j++){
            arr3[j][i] = arr1[i][j]
        }
    }

</script>

<div class="container">
    <div class="n2-q4">
        <h2>
            4 - Implementar uma página que, dados dois arrays bidimensionais, escreve no segundo array a transcrição do primeiro.
        </h2>

        <div class="titulo-tabela">
            <h3>Elementos do Array 1 :</h3>
            <table class="tabela">
                {#each arr1 as linha}
                    <tr>
                        {#each linha as coluna}
                            <td>{coluna}</td>
                        {/each}
                    </tr>
                {/each}
            </table>
        </div>
        <div class="titulo-tabela">
            <h3>Elementos do Array 2 :</h3>
            <table class="tabela">
                {#each arr2 as linha}
                    <tr>
                        {#each linha as coluna}
                            <td>{coluna}</td>
                        {/each}
                    </tr>
                {/each}
            </table>
        </div>
        <div class="titulo-tabela">
            <h3 class="saida">Saída ( array 2 ) :</h3>
            <table class="tabela">
                {#each arr3 as linha}
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
    <a class="botao" href="/nivel 2">Voltar</a>
</div>