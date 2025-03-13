## Axios
- Quando utilziamos
- Conceitos básicos

```js
import React from 'react'
import axios from 'axios'

const App = () => {
    //API 
    const Buscar = async () => {
        const url = "http://viacep.com.br/ws/17050790/json/"
        await axios.get( url )
            .then( retorno => {
                console.log( retorno )
            })
            .catch( erro => {

            })

        console.log("oi")
    }

    return (
        <div> <input type='button' value='buscar' onClick={ () => Buscar() } />
        </div>
    )
}

export default App
```
