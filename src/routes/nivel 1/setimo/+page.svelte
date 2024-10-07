<script lang="ts">

    // Implementar uma página que, dados dois arrays bidimensionais, exibe true se ambos forem iguais ou false caso contrário;

    let arr1:number[][] = [[1,2,3],[4,5,6],[7,8,9]] 
    let arr2:number[][] = [[1,2,3],[4,5,6],[7,8,9]]
    let verificação:boolean = false
    let cont:number = 0
    let element:number = 0

    for(let i:number = 0 ; i < arr1.length ; i++){
        for( let j:number = 0 ; j < arr1[i].length ; j++ ){
            element++
            if(arr1[i][j] == arr2[i][j]){
                cont++
            }
        }
    }

    if(cont == element){
        verificação = true
    }

</script>

<div class="container">
    <div class="n1-q7">
        <h2>
            7 - Implementar uma página que, dados dois arrays bidimensionais, exibe true se ambos forem iguais ou false caso contrário.
        </h2>
        
        <div class="titulo-tabela">
            <h3>Elementos do array 1 :</h3>
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
            <h3>Elementos do array 2 :</h3>
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
        <h3 class="saida">Saida: {verificação}</h3>
    </div>
</div>

<div class="voltar">
    <a class="botao" href="/nivel 1">Voltar</a>
</div>
