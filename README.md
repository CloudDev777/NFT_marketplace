# `ethereum-NFT-Marketplace`

This project work on any EVM-compatible blockchain such as Polygon, Avalanche, Binance Smart Chain and other such chains.

![Preview](preview.gif)

   


✏ Rename `.env.example` to `.env` in the main folder and provide your `appId` and `serverUrl` from Moralis ([How to start Moralis Server](https://docs.moralis.io/moralis-server/getting-started/create-a-moralis-server)) 
Example:
```jsx
REACT_APP_MORALIS_APPLICATION_ID = xxxxxxxxxxxx
REACT_APP_MORALIS_SERVER_URL = https://xxxxxx.grandmoralis.com:2053/server
```

🔎 Locate the MoralisDappProvider in `src/providers/MoralisDappProvider/MoralisDappProvider.js` and paste the deployed marketplace smart contract address and ABI
```jsx
const [contractABI, setContractABI] = useState();
const [marketAddress, setMarketAddress] = useState();
```

🔃 Sync the `MarketItemCreated` event `/src/contracts/marketplaceBoilerplate.sol` contract with your Moralis Server, making the tableName `MarketItems`
```jsx
event MarketItemCreated (
  uint indexed itemId,
  address indexed nftContract,
  uint256 indexed tokenId,
  address seller,
  address owner,
  uint256 price,
  bool sold
);
```


🚴‍♂️ Run your App:
```sh
yarn start
```


