<script lang="ts">
    
    // Implementar uma página que exibe a quantidade de elementos ímpares em um array de duas dimensões;

    let arr:number[][] = [[1,2,3],[4,5,6],[7,8,9]]
    let cont:number = 0

    for(let i:number = 0;i<arr.length;i++){
        for(let j:number = 0;j<arr[i].length;j++){    
            if(arr[i][j] %2 == 1){
                cont++
            }
        }
    }

</script>

<div class="container">
    <div class="n1-q3">
        <h2>
            3 - Implementar uma página que exibe a quantidade de elementos ímpares em um array de duas dimensões.
        </h2>
        
        <div class="titulo-tabela">
            <h3>Elementos do Array :</h3>
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
        <h3 class="saida">Saida: {cont}</h3>
    </div>
</div>
<div class="voltar">
    <a class="botao" href="/nivel 1">Voltar</a>
</div>


