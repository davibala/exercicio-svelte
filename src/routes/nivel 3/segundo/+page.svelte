<script lang="ts">

    // Implementar uma página capaz de imprimir as diagonais de array tridimensional, sem usar laços

    let arr:number[][][] = [
        [
            [1, 2, 3],
            [4, 5, 6],
            [7, 8, 9]
        ],
        [
            [10, 11, 12],
            [13, 14, 15],
            [16, 17, 18]
        ],
        [
            [19, 20, 21],
            [22, 23, 24],
            [25, 26, 27]
        ]
    ];

    let n:number = arr.length;

    let diagonais:number[][] = [[],[],[],[]]
    
    function DiagonalPrimaria(arr:number[][][],dp:number[],i:number = 0):number[]{
        if(i>=arr.length){
            return dp
        }
        dp[i] = arr[i][i][i]
        return DiagonalPrimaria(arr,dp, i + 1)
    }

    function DiagonalSecundaria(arr:number[][][],ds:number[],i:number = 0):number[]{
        if(i>=arr.length){
            return ds
        }
        ds[i] = arr[i][i][n - i - 1]
        return DiagonalSecundaria(arr,ds, i + 1)
    }

    function DiagonalTerciaria(arr:number[][][],dt:number[],i:number = 0):number[]{
        if(i>=arr.length){
            return dt
        }
        dt[i] = arr[i][n - i - 1][i]
        return DiagonalTerciaria(arr,dt, i + 1)
    }

    function DiagonalQuaternaria(arr:number[][][],dq:number[],i:number = 0):number[]{
        if(i>=arr.length){
            return dq
        }
        dq[i] = arr[i][n - i - 1][n - i - 1]
        return DiagonalQuaternaria(arr,dq, i + 1)
    }

</script>

<div class="container">
    <div class="n3-q1">
        <h2>
            2 - Implementar uma página capaz de imprimir as diagonais de array tridimensional, sem uso de laços.
        </h2>   
        <div id="idn3q1">
            <h3>Elementos do Array:</h3>
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
        
        <ul>
            <li><h3>Diagonal principal: {DiagonalPrimaria(arr,diagonais[0])}</h3></li>
            <li><h3>Diagonal secundária: {DiagonalSecundaria(arr,diagonais[1])}</h3></li>
            <li><h3>Diagonal terciária: {DiagonalTerciaria(arr,diagonais[2])}</h3></li>
            <li><h3>Diagonal quaternária: {DiagonalQuaternaria(arr,diagonais[3])}</h3></li>
        </ul>
    </div>
</div>

<div class="voltar">
    <a class="botao" href="/nivel 3">Voltar</a>
</div>