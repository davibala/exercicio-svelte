<script lang="ts">
    
    import '../../../styles/global.css'

    let array:number[][] = [[1,2,3],[4,5,6],[7,8,9]]
    let n:number = 10
    let newarray:number[][] = [[],[],[]]

    for(let i:number = 0;i<array.length;i++){
        for(let j:number = 0;j<array[i].length;j++){
            newarray[i][j] = array[i][j] * n
        }
    }

</script>

<div class="container">
    <h2>
        1 - Implementar uma página que, dado um array bidimensional e um número, multiplica cada elemento do array pelo número.
    </h2>
    <div class="n1-q1">

        <div id="q1">
            <h3>Nosso número : {n}</h3>
            
            <div class="titulo-tabela">
                <h3>Nosso Array :</h3>
                <table class="tabela">
                    {#each array as linha}
                        <tr>
                            {#each linha as coluna}
                                <td>{coluna}</td>
                            {/each}
                        </tr>
                    {/each}
                </table>
            </div>
        </div>
        <div class="titulo-tabela">
            <h3 class="saida">Saída :</h3>
        
            <table class="tabela">
                {#each newarray as linha}
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
    <a class="botao" href="/nivel 1">Voltar</a>
</div>
