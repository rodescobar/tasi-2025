## Aplicação de CSS em calculadora

- Utilização de envio de informações do objeto Filho -> Pai


```App.js
//App.js
import React from 'react'
import Filho from './Filho'

const estilos = {
    fundo: {
        width: "410px",
        backgroundColor: "black",
        color: "white",
        border: "1px solid #ccc",
        borderRadius: "10px",
        display: "flex"
    },
    parteSuperior: {
        width: "410px"
    },
    formula: {
        fontSize: "38px",
        color: "#ccc",
        textAlign: "right",
        padding: "10px"
    },
    numero: {
        fontSize: "54px",
        color: "white",
        textAlign: "right",
        padding: "10px"
    },
    botoes: {
        width: "410px",
        height: "510px",
        display: "flex"
    },
    caixa: {
        width: "410px",
        height: "100px",
        backgroundColor: "black",
        display: "flex",
        direction: "column"
    }
}

const App = () => {
    const Recebe = (valor) => {
        var formula = " 5 + 8 * 9 - 6 + 36 "
        var resultado = eval(formula)
        console.log(resultado)
    }

    return (
        <div style={estilos.fundo}>
            <div style={{ display: "inline" }}>
                <div style={estilos.parteSuperior}>
                    <div style={estilos.formula}>
                        5*9+8/3-98
                    </div>
                    <div style={estilos.numero}>
                        78
                    </div>
                </div>

                <div style={estilos.botoes}>
                    <div style={ { direction: "row" }}>
                        <Filho valor="AC" cor="gray" callback={ Recebe } />
                        <Filho valor="7" cor="gray" callback={ Recebe } />
                        <Filho valor="4" cor="gray" callback={ Recebe } />
                        <Filho valor="1" cor="gray" callback={ Recebe } />
                        <Filho valor=" " cor="gray" callback={ Recebe } />
                    </div>
                    <div style={ { direction: "row" }}>
                        <Filho valor="+/-" cor="gray" callback={ Recebe } />
                        <Filho valor="8" cor="gray" callback={ Recebe } />
                        <Filho valor="5" cor="gray" callback={ Recebe } />
                        <Filho valor="2" cor="orange" callback={ Recebe } />
                        <Filho valor="0" cor="orange" callback={ Recebe } />
                    </div>
                </div>
            </div>
        </div>
    )
}

export default App
```

```Filho.js
//Filho.js
import React from 'react'

const Filho = ({ valor, cor, callback }) =>{

    const Clique = () => {
        callback( valor )
    }

    return (
        <div style={ {
            backgroundColor: cor,
            borderRadius: "50px",
            width: "100px",
            height: "100px",
            display: "flex",
            flexDirection: "column",
            justifyContent: "center",
            alignItems: "center"
        } }
            onClick={ () => Clique() }
        >
            { valor }
        </div>
    )
}

export default Filho
```
