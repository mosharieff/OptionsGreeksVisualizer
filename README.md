# Options Greeks Visualizer

## Disclaimer
This program should in no way, shape, or form be used for actual trading. This program was created for purely Quantitative Finance and Math methods. Plus the data takes long to load in the visualizer, and options greeks fluctuate very quick to be sitting around using this program.

## Instructions
In order to get this program running you will need to have Node, NPM and React.js installed (there are many tutorials online for installing on the Windows, Mac, or Linux). Additionally you will need the python libraries aiohttp, websockets, numpy, and scipy installed.

#### Installation
```sh
pip install -r requirements.txt
npm install --force
```

## Running
To run this app you need to navigate to its root directly and open two terminals. In the first terminal type in ``` python server``` and in the second terminal type in ``` npm start```

Once the server and web app are open (in seperate terminals), you will be able to type in a number into the Number of Stocks input and a set of input holders will be generated, in which you enter each individual stock. Once you have entered your stock tickers press the blue button up top "Options Greeks Visualizer" and it will import all of the options greeks graphs for you.

## Rate Limits
This apps payload is very heavy and will require lots of requests. I would advise you to use a max of three to five stocks in the visualizer as to not get ratelimited.

## Programs Methods
1. Sends a request to fetch the latest Treasury Yields to be used as the risk free rates
2. Recieves a list of tickers to fetch for the visualization
3. Fetches options chain data in order to extract the expirations list
4. Sends mass asynchronus request to get all of the options data
5. Implied volatility and expiry are then used to match the correct treasury rate to the calculations by matching expiry dates
6. Additionally the dividend yield is imported as well and all of the inputs are pushed through the trinomial tree and greeks are returned.

## Greek Visuals

### Implied Volatility Graphs
![alt](https://github.com/mosharieff/OptionsGreeksVisualizer/blob/main/images/IV.png)

### Delta
![alt](https://github.com/mosharieff/OptionsGreeksVisualizer/blob/main/images/Delta.png)

### Gamma
![alt](https://github.com/mosharieff/OptionsGreeksVisualizer/blob/main/images/Gamma.png)

### Theta
![alt](https://github.com/mosharieff/OptionsGreeksVisualizer/blob/main/images/Theta.png)

### Vega
![alt](https://github.com/mosharieff/OptionsGreeksVisualizer/blob/main/images/Vega.png)

### Rho
![alt](https://github.com/mosharieff/OptionsGreeksVisualizer/blob/main/images/Rho.png)
