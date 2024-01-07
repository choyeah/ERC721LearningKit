# env

```
PUBLIC_KEY=''
TEST_PUBLIC_KEY=''
PRIVATE_KEY=''
TEST_PRIVATE_KEY=''
ERC721=''
RPC_URL='https://rpc.holesky.ethpandaops.io'
RPC_URL_HOLESKY='https://rpc.holesky.ethpandaops.io'
```

# metadat

1. metadata url

```
https://docs.opensea.io/docs/metadata-standards
```

```
{
  "description": "Fastcampus X 체인의정석.",
  "image": "https://raw.githubusercontent.com/choyeah/ERC721LearningKit/metadata/image.png",
  "name": "NFT example"
}
```

# truffle ERC721

1. 컨트렉트배포

```
truffle migrate --network holesky
```

2. 테스트 진행

   Start local network (로컬 네트워크 실행)

   ```
   truffle develop
   ```

   run erc721 test (Erc20 단위 테스트 파일 실행)

   ```
   truffle(develop)> test ./test/ERC721.js
   ```

3. 함수 실행

잔고 조회

```
node scripts/balanceOfERC721.js --network holesky
```

민팅

```
node scripts/mint.js --network holesky
```

전송

```
node scripts/transferERC721.js --network holesky
```

이벤트 조회

```
node scripts/events.js --network holesky
```

# hardhat ERC721

1. 컨트렉트 배포

```
npx hardhat run scripts/deploy.ts
```

2. 컨트렉트 테스트

   run erc721 test (Erc721 단위 테스트 파일 실행)

   ```
   npx hardhat test test/erc721Test.ts
   ```

   run scenario erc721 test (Erc721 시나리오 테스트 파일 실행)

   ```
   npx hardhat test test/erc721ScenarioTest.ts
   ```

3. 함수 실행
   민팅
   ```
   npx hardhat run scripts/mint.ts --network holesky
   ```
   조회
   ```
   npx hardhat run scripts/getBalance.ts --network holesky
   ```
   전송
   ```
   npx hardhat run scripts/transfer.ts --network holesky
   ```
   이벤트 조회
   ```
   npx hardhat run scripts/event.ts --network holesky
   ```
