# SafeChain

Простий запуск проєкту.

## Що потрібно заздалегідь

- Windows
- Node.js 18+
- Solana CLI
- Anchor CLI
- Phantom 

Перевірка:

- `node -v`
- `solana --version`
- `anchor --version`

---

## Швидкий запуск (рекомендовано)

У корені проєкту:

1. `npm install`
2. `npm run dev:box`

Після запуску:

- Frontend: http://localhost:5173
- Backend: http://localhost:8080
- Localnet RPC: http://127.0.0.1:8899

---

## Якщо хочеш запускати вручну

### 1) Встановити залежності

- У корені: `npm install`
- Frontend: `npm --prefix app/frontend install`
- Backend: `npm --prefix backend install`

### 2) Зібрати програму

- `anchor build --no-idl`

### 3) Запустити local validator

- `solana-test-validator --ledger ./test-ledger -r`

### 4) Задеплоїти програму

- `solana program deploy target/deploy/safechain.so --program-id target/deploy/safechain-keypair.json --url http://127.0.0.1:8899`

### 5) Запустити backend

- `npm --prefix backend run dev`

### 6) Запустити frontend

- `npm --prefix app/frontend run dev`

---

## Корисні команди

- Зробити backup ключа програми:
  - `npm run backup:critical`

- Очистити важкі папки (target/test-ledger/node_modules/dist):
  - `npm run clean:heavy`

- Запустити все однією командою після очистки:
  - `npm run dev:box`

---



