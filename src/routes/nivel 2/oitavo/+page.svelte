<script lang="ts">

    // Implementar uma página que, dado um array bidimensional, atribui 0 a todos os elementos presentes em suas diagonais.

    let arr:number[][] = [
        [1,2,3,4,5],
        [6,7,8,9,10],
        [11,12,13,14,15],
        [16,17,18,19,20],
        [21,22,23,24,25],
    ]

    let arr2:number[][] = [
        [1,2,3,4,5],
        [6,7,8,9,10],
        [11,12,13,14,15],
        [16,17,18,19,20],
        [21,22,23,24,25],
    ]
    
    let cont:number = 0

    for(let i:number = 0;i<arr.length;i++){             // susbtitui os elementos na diagonal, da esquerda pra direita.
        for(let j:number = cont;j<arr[i].length;j++){
            arr[i][cont] = 0
        }
        cont++
    }

    let cont2:number = arr[1].length -1

    for(let i:number = 0;i<arr.length;i++){             // susbtitui os elementos na diagonal, da direita pra esquerda.
        for(let j:number = cont;j>0;j--){
            arr[i][cont2] = 0
        }
        cont2--
    }

</script>

<div class="container">
    <div class="n2-q8">
        <h2>
            8 - Implementar uma página que, dado um array bidimensional, atribui 0 a todos os elementos presentes em suas diagonais.
        </h2>

        <div class="titulo-tabela">
            <h3>Elementos do Array:  </h3>
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
            <h3 class="saida">Saída:</h3>
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
</div>
    
<div class="voltar">
    <a class="botao" href="/nivel 2">Voltar</a>
</div>
    
    