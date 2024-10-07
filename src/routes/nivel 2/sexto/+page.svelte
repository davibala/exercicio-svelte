<script lang="ts">

    // Implementar uma página que, dados dois arrays bidimensionais, retorna qual deles possui a maior soma de seus elementos;

    let arr1:number[][] = [
        [1,2,3],
        [4,5,6],
        [7,8,9],
    ]

    let arr2:number[][] = [
        [12,3,4],
        [5,6,7],
        [8,9,10],
    ]

    let result:string = ""


    function SomaElementos(arr:number[][]):number{
        let soma:number = 0

        for(let i:number = 0;i<arr.length;i++){
            for(let j:number = 0;j<arr[i].length;j++){
                soma += arr[i][j]
            }
        }
        return soma
    }

    if(SomaElementos(arr1)>SomaElementos(arr2)){
        result = "Array 1"
    } else if(SomaElementos(arr1)<SomaElementos(arr2)) {
        result = "Array 2"
    } else {
        result = "somas iguais"
    }

</script>

<div class="container">
    <div class="n2-q6">

        <h2>
            6 - Implementar uma página que, dados dois arrays bidimensionais, retorna qual deles possui a maior soma de seus elementos.
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

        <h3 class="saida">Saída : {result}</h3>
    </div>
</div>

<div class="voltar">
    <a class="botao" href="/nivel 2">Voltar</a>
</div>



