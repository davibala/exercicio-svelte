<script lang="ts">

    // Implementar uma página que, dado um array bidimensional, computa a média dos seus elementos, conta e retorna quantos elementos acima da média ele possui;

    let arr:number[][] = [
        [1,2,3],
        [4,5,6],
        [7,8,9],
    ]

    let soma:number = 0
    let cont1:number = 0
    let cont2:number = 0

    for(let i:number = 0;i<arr.length;i++){
        for(let j:number = 0;j<arr[i].length;j++){
            soma += arr[i][j]
            cont1++
        }
    }

    let media:number = soma / cont1

    for(let i:number = 0;i<arr.length;i++){
        for(let j:number = 0;j<arr[i].length;j++){
            if(arr[i][j] > media){
                cont2++
            }
        }
    }



</script>

<div class="container">
    <div class="n2-q7">
        <h2>
            7 - Implementar uma página que, dado um array bidimensional, computa a média dos seus elementos, conta e retorna quantos elementos acima da média ele possui.
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

        <h3 class="saida">Saida: {cont2}</h3>

    </div>
</div>

<div class="voltar">
    <a class="botao" href="/nivel 2">Voltar</a>
</div>
