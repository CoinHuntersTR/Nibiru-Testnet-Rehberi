# Nibiru’da bir akıllı sözleşme dağıtın.

### Akıllı Kontrat Görevleri - Kontrat Deploy

![Nibiru Teşvikli Test Ağı](https://user-images.githubusercontent.com/107190154/230292010-0829ac0c-b088-4354-96cb-5aa236465060.png)


## Adımları sırasıyla yaparsanız sorunsuz şekilde yaparsınız.

### Terminali açın ve aşağıdaki komutla nibid binary’i yükleyin. Bu, Nibiru CLI uygulamasını barındırır.
**Not: Bu işlemi Nibiru'nun kurulu olmadığı bir sunucuda da yapabilirsiniz.**

```
curl -s https://get.nibiru.fi/! | bash
```
```
nibid config node https://rpc.itn-1.nibiru.fi:443
nibid config chain-id nibiru-itn-1
nibid config broadcast-mode block
nibid config keyring-backend file
```

## Bir klasör oluşturuyoruz ve buraya `cw1_whitelist.wasm` dosyamızı çekiyoruz.

```
mkdir nibidcontract
cd nibidcontract
wget https://github.com/NibiruChain/cw-nibiru/raw/main/artifacts-cw-plus/cw1_whitelist.wasm
```

## `nibidcontract` klasörümüze giriyoruz ve değişkenleri ayarlıyoruz.

```
cd $HOME/nibidcontract
KEY_NAME="CÜZDANADINIZ"
CONTRACT_WASM="$HOME/nibidcontract/cw1_whitelist.wasm"
```

## Kontrat Dağıtma adımı.

```
nibid tx wasm store $CONTRACT_WASM --from $KEY_NAME --gas=2000000 --fees=50000unibi
```


## İşlemi onaylamak için `y` basın ve enterlayın.
> `code id` ve `txhash` bir yere not edin.



### Örnek Çıktı:
```
code: 0
codespace: ""
data: 0A470A1E2F636F736D7761736D2E7761736D2E76312E4D736753746F7265436F646512250897021220A1E2AA264EA3E9D6F1D59D10DED2C6D72BA741C5D8E6999A41EC3F2E6B4C7741
events:
- attributes:
  - index: true
    key: c3BlbmRlcg==
    value: bmliaTF4eG42dGdkYzc1Z2RoOWw5dGx2bmN5NDVkeXRzaGt2eGNsMG02YQ==
  - index: true
    key: YW1vdW50
    value: NTAwMDB1bmliaQ==
  type: coin_spent
- attributes:
  - index: true
    key: cmVjZWl2ZXI=
    value: bmliaTE3eHBmdmFrbTJhbWc5NjJ5bHM2Zjg0ejNrZWxsOGM1bDh1OGV6dw==
  - index: true
    key: YW1vdW50
    value: NTAwMDB1bmliaQ==
  type: coin_received
- attributes:
  - index: true
    key: cmVjaXBpZW50
    value: bmliaTE3eHBmdmFrbTJhbWc5NjJ5bHM2Zjg0ejNrZWxsOGM1bDh1OGV6dw==
  - index: true
    key: c2VuZGVy
    value: bmliaTF4eG42dGdkYzc1Z2RoOWw5dGx2bmN5NDVkeXRzaGt2eGNsMG02YQ==
  - index: true
    key: YW1vdW50
    value: NTAwMDB1bmliaQ==
  type: transfer
- attributes:
  - index: true
    key: c2VuZGVy
    value: bmliaTF4eG42dGdkYzc1Z2RoOWw5dGx2bmN5NDVkeXRzaGt2eGNsMG02YQ==
  type: message
- attributes:
  - index: true
    key: ZmVl
    value: NTAwMDB1bmliaQ==
  type: tx
- attributes:
  - index: true
    key: YWNjX3NlcQ==
    value: bmliaTF4eG42dGdkYzc1Z2RoOWw5dGx2bmN5NDVkeXRzaGt2eGNsMG02YS84OTI1
  type: tx
- attributes:
  - index: true
    key: c2lnbmF0dXJl
    value: L1hRYlhNSXJuUGZ2NmZHWlFmOE8vbmkwdy90QUhpTGZZekc5d3hRcmNpRkdlWVZMOHFuVXpwMWxCYVA3dEtoVnlkZERBVVdJdFpZQTY5K2tGdzJXS0E9PQ==
  type: tx
- attributes:
  - index: true
    key: YWN0aW9u
    value: L2Nvc213YXNtLndhc20udjEuTXNnU3RvcmVDb2Rl
  type: message
- attributes:
  - index: true
    key: bW9kdWxl
    value: d2FzbQ==
  - index: true
    key: c2VuZGVy
    value: bmliaTF4eG42dGdkYzc1Z2RoOWw5dGx2bmN5NDVkeXRzaGt2eGNsMG02YQ==
  type: message
- attributes:
  - index: true
    key: Y29kZV9jaGVja3N1bQ==
    value: YTFlMmFhMjY0ZWEzZTlkNmYxZDU5ZDEwZGVkMmM2ZDcyYmE3NDFjNWQ4ZTY5OTlhNDFlYzNmMmU2YjRjNzc0MQ==
  - index: true
    key: Y29kZV9pZA==
    value: Mjc5
  type: store_code
gas_used: "1426576"
gas_wanted: "2000000"
height: "1654067"
info: ""
logs:
- events:
  - attributes:
    - key: action
      value: /cosmwasm.wasm.v1.MsgStoreCode
    - key: module
      value: wasm
    - key: sender
      value: nibi1xxn6tgdc75gdh9l9tlvncy45dytshkvxcl0m6a
    type: message
  - attributes:
    - key: code_checksum
      value: a1e2aa264ea3e9d6f1d59d10ded2c6d72ba741c5d8e6999a41ec3f2e6b4c7741
    - key: code_id
      value: "279"
    type: store_code
  log: ""
  msg_index: 0
raw_log: '[{"events":[{"type":"message","attributes":[{"key":"action","value":"/cosmwasm.wasm.v1.MsgStoreCode"},{"key":"module","value":"wasm"},{"key":"sender","value":"nibi1xxn6tgdc75gdh9l9tlvncy45dytshkvxcl0m6a"}]},{"type":"store_code","attributes":[{"key":"code_checksum","value":"a1e2aa264ea3e9d6f1d59d10ded2c6d72ba741c5d8e6999a41ec3f2e6b4c7741"},{"key":"code_id","value":"279"}]}]}]'
timestamp: ""
tx: null
txhash: 11A3D0045FCD92BC453CE2D439305D25DDA0609C2DA85CD33DB840C9B2556D67
```

## `code id` ve `txhash` bir yere not edin.


### `Code Id` bilgilerinizi öğrenmek için aşağıdaki komutu kullanın.
```
nibid query wasm code-info CODEIDYAZIN
```

### Örnek Komut:
```
nibid query wasm code-info 279
```

### Herhangi bir sorunuz varsa, discord'da sorabilirsiniz : [Discord](https://discord.gg/H2b69CFqrK)

### CoinHunters Telegram : [Telegram](https://t.me/CoinHuntersTR/34102) 
