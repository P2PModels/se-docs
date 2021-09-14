# Decentralized Applications (dapps)

Una dapp es una aplicación que funciona principalmente o enteramente de manera
descentralizada. Las principales ventajas de una dapp sobre soluciones centralizadas
son: la resilencia debido a que la lógica de la aplicación puede ser distribuida 
en la red P2P; la transparencia debido a que al estar el código de la lógica de
la aplicación alojado en la blockchain se puede acceder al mismo inspeccionando
la blockchain (siempre que esta sea pública como la mainnet de Ethereum); y 
resistencia a censura ya la naturalez distrubuida de la red sobre la que opera
la aplicación hace que cualquier usuario pueda interactuar con la lógica de la
aplicación sin interferencia de una autoridad central.

![Decentralized Pic](../figures/dcap_0101.png)

## Backend

El backend de las dapps son los smart contracts que se encargan de almacenar
toda la lógica de la aplicación. Un aspecto a considerar en el desarrollo de 
smart contracts es la imposibilidad de cambiar el código una vez este ha sido
desplegado en la blockchain.

## Frontend

El frontend de las dapps pueden estar implementados usando tecnología web
estándar (HTML, CSS, Javascript) a diferencia del backend que es desarrollado a 
través de los smart contracts.

### Web3

Normalmente el frontend de una dapp interactua con Ethereum a través de una
librería javascript llamada [Web3](https://web3js.readthedocs.io/en/v1.5.2/). 
Web3 se encarga de gestionar el acceso a nodos locales o remotos de ethereum,
así como también se ocupa de la interacción con las wallets.

### React

[React](https://reactjs.org) es en la actualidad uno de los frameworks de 
desarrollo de interfaces webs más extendidos y utilizados. Creado por Facebook 
ofrece un tooling de herramientas que facilita la gestión de los componentes y 
el estado de la aplicación.
