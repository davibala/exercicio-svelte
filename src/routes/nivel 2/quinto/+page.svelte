<script lang="ts">

    // Implementar uma página que, dado um array tridimensional, computa a média de seus elementos;

    let arr:number[][][] = [
        [
            [10,10,10],
            [10,10,10],
            [10,10,10]
        ],
        [
            [20,20,20],
            [20,20,20],
            [20,20,20]
        ],
        [
            [30,30,30],
            [30,30,30],
            [30,30,30]
        ]
    ]

    let soma:number = 0
    let cont:number = 0

    for(let i:number = 0;i<arr.length;i++){
        for(let j:number = 0;j<arr[i].length;j++){
            for(let k:number = 0;k<arr[i][j].length;k++){
                soma += arr[i][j][k] // soma os elementos
                cont++ // conta a quantidade de elementos
            }
        }
    }


    let media:number = soma / cont


</script>

<div class="container">
    <div class="n2-q5">

        <h2> 5 - Implementar uma página que, dado um array tridimensional, computa a média de seus elementos. </h2>

        <div id="idn2q5">
            <h3>Elementos do array :</h3>
            <div class="titulo-tabela">
                {#each arr as page }
                    <table class="tabela">
                        {#each page as linha }
                            <tr>
                                {#each linha as coluna }
                                    <td>{coluna}</td>
                                {/each}
                            </tr>
                        {/each}
                    </table><br>
                {/each}
            </div>
        </div>

        <h3 class="saida">Saída: {media} </h3>
    
    </div>
</div>

<div class="voltar">
    <a class="botao" href="/nivel 2">Voltar</a>
</div>
