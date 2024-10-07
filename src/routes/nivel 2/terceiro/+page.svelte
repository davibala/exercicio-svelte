<script lang="ts">

    // Implementar uma página que, dados três arrays bidimensionais, guarda no terceiro array a soma dos índices equivalentes no dois primeiros;
    // Exemplo: c[1][2] = a[1][2] + b[1][2]; // e assim por diante

    let arr1:number[][] = [[1,2,3],[4,5,6],[7,8,9]]
    let arr2:number[][] = [[9,8,7],[6,5,4],[3,2,1]]
    let arr3:number[][] = [[0,0,0],[0,0,0],[0,0,0]]

    for(let i:number = 0;i<(arr1.length > arr2.length ? arr1.length : arr2.length);i++){
        for(let j:number = 0;j<(arr1.length > arr2.length ? arr1[i].length : arr2[i].length);j++){
            arr3[i][j] = arr1[i][j] + arr2[i][j]
        }
    }

</script>


<div class="container">
    <div class="n2-q3">
        <h2>
            3 - Implementar uma página que, dados três arrays bidimensionais, guarda no terceiro array a soma dos índices equivalentes no dois primeiros.
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
            <h3 class="saida">Saída ( Array 3 ):</h3>
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




