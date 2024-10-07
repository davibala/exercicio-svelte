<script lang="ts">

    // Implementar uma página que, dados dois arrays bidimensionais, copia o conteúdo do primeiro no segundo array;

    let arr1:number[][] = [[1,0,1],[0,1,0],[1,0,1]]
    let arr2:number[][] = [[0,0,0],[0,0,0],[0,0,0]]
    let arr3:number[][] = [[0,0,0],[0,0,0],[0,0,0]]


    for(let i:number = 0;i<arr1.length;i++){
        for(let j:number = 0;j<arr1[i].length;j++){
            arr3[i][j] = arr1[i][j]
        }
    }


</script>

<div class="container">
    <div class="n2-q2">
        <h2>
            2 - Implementar uma página que, dados dois arrays bidimensionais, copia o conteúdo do primeiro no segundo array.
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


