<script lang="ts">
    
    
    // Implementar uma página que, dadas a quantidade de linhas e de colunas, cria um array de duas dimensões com a quantidade de linhas e colunas especificadas, inicializa seus índices com o valor -1, o imprime e o retorna;

    let linhas: number = 5;
    let colunas: number = 5;

    function ImprimePadrao(linhas: number,colunas: number,indices: number): number[][] {
        
        let array: number[][] = [[]];

        for (let i: number = 0; i < linhas; i++) {
            array[i] = [];
            for (let j: number = 0; j < colunas; j++) {
                array[i][j] = indices;
                indices++;
            }
        }

        return array;
    }
</script>
<div class="container">
    <div class="n2-q1">

        <h2>
            1 - Implementar uma página que, dadas a quantidade de linhas e de colunas, cria um array de duas dimensões com a quantidade de linhas e colunas especificadas, inicializa seus índices com o valor -1, o imprime e o retorna.
        </h2>
        <div id="idn2q1">
            <h3>Linhas: {linhas}</h3>
            <h3>Colunas: {colunas}</h3>
        </div>

        <div class="titulo-tabela">
            <h3 class="saida">Saída:</h3>
            <table class="tabela">
                {#each ImprimePadrao(linhas, colunas, -1) as linha}
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


