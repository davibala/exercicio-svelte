<script lang="ts">

    // Implementar uma página que, dados um array bidimensional de booleans, imprime true se ao menos um dos elementos do array forem verdadeiros ou false, caso contrário.

    let arr:boolean[][] = [[false,false,false],[false,true,false],[false,false,false]]
    let verificação:boolean = false

    for(let i:number = 0;i<arr.length;i++){
        for(let j:number = 0;j<arr[i].length;j++){
            if(arr[i][j] == true){
                verificação = true
            }
        }
    }

</script>

<div class="container">
    <div class="n1-q8">
        <h2>
            8 - Implementar uma página que, dados um array bidimensional de booleans, imprime true se ao menos um dos elementos do array forem verdadeiros ou false, caso contrário.
        </h2>

        <div class="titulo-tabela">
            <h3>Elementos do array: </h3>
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
        <p class="saida">Saída: {verificação}</p>
    </div>
</div>

<div class="voltar">
    <a class="botao" href="/nivel 1">Voltar</a>
</div>




