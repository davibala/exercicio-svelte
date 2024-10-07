<script lang="ts">

    // Implementar uma página que, dado um array bidimensional, exibe true se a soma dos seus elementos for positiva ou false, caso contrário;

    let arr:number[][] = [[1,2,3],[4,5,6],[7,8,9]]
    let soma:number = 0
    let verificação:boolean = false

    for(let i:number = 0;i< arr.length;i++){
        for(let j:number= 0;j<arr[i].length;j++){
            soma += arr[i][j]
        }
    }
    if(soma>0){
        verificação = true
    }

</script>

<div class="container">
    <div class="n1-q2">
        <h2>
            2 - Implementar uma página que, dado um array bidimensional, exibe true se a soma dos seus elementos for positiva ou false, caso contrário.
        </h2>
    
        <div class="titulo-tabela">
            <h3>
                Elementos do Array : 
            </h3>
            
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
        
        <h3 class="saida">Saída: {verificação}</h3>

    </div>
</div>

<div class="voltar">
    <a class="botao" href="/nivel 1">Voltar</a>
</div>