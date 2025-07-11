# CoTrain - AI��s�

## y��

CoTrain/ *��:W��AI��s���Aptos�/�-��O\AI!���

## �/

### ��
- **Monorepo**: (pnpm workspaces���
- **�h**: pnpm (�{(pnpm�(npmyarn)

### M�/
- **F�**: Next.js 15.2.4 (App Router)
- **UI�**: HeroUI 2.7.11 (;�) + shadcn/ui (���)
- **ReactH,**: React 18.3.1 (|�'Q)
- **7**: Tailwind CSS 3.4.17
- **�;**: Framer Motion 12.23.0
- **��**: Zustand 5.0.6
- **hU**: React Hook Form 7.59.0 + Zod 3.25.67
- **pn��**: TanStack Query 5.81.5
- **;�**: next-themes 0.4.6
- **�h**: Recharts 2.15.0
- **�**: Lucide React 0.454.0

### �/
- **F�**: NestJS
- **pn�**: PostgreSQL (Docker�h)
- **X**: Redis (Docker�h)
- **ORM**: TypeORM
- **��**: JWT + Passport
- **��**: Bull Queue
- **��**: EventEmitter
- **�**: @nestjs/schedule
- **�c**: Swagger/OpenAPI

### :W��/
- **:W�**: Aptos Testnet
- **SDK**: @aptos-labs/ts-sdk 1.39.0
- **�Mh**: @aptos-labs/wallet-adapter-react 6.1.2
- **/�**: 
  - Aptos���
  - Petra�
  - Martian�
  - MSafe�
  - �*JM�
  - SolanaM�

###  ��w
- **TypeScript**: 5.8.3
- **ESLint**: 8.57.1
- **Prettier**: 3.6.2
- **Autoprefixer**: 10.4.21
- **PostCSS**: 8.5.6

### P2PQ܌AI��
- **P2PQ�**: �IP2PQ��
- **��Z**: ��Z��
- **!.�***: z�� + ,0�*
- **V��**: �V����
- **DHT�**: �h�

## y�ӄ

```
co-train_aptos/
   apps/
      frontend/               # Next.jsM�(
         src/
            app/           # App Routerub
            components/    # React��
               heroui/    # HeroUI���
               cotrain/   # y�y���
               shared/    # q���
            contexts/      # React Context
            hooks/         # �IHooks
            lib/           # �w�p
            types/         # TypeScript{��I
         next.config.mjs    # Next.jsMn
         tailwind.config.ts # TailwindMn
         package.json
      backend/               # NestJS�API
          src/
             modules/       # �!W
                auth/      # ��!W
                users/     # (7�
                training/  # ����
                blockchain/ # :W��
                hivemind/  # P2PQ܌AIO
                websocket/ # ���
             config/        # Mn��
             database/      # pn���
             common/        # q��
          package.json
   packages/                  # q�
      shared-types/         # q�{��I
      shared-utils/         # q��w�p
      shared-config/        # q�Mn
   docker-compose.yml        # Docker��
   pnpm-workspace.yaml      # pnpm�\z�Mn
   package.json             # 9Mn
   CLAUDE.md               # ,��

```

##  �}�

### y��
```bash
# �ŝV (�{(pnpm)
pnpm install

# /�pn��
docker-compose up -d postgres redis

# �pn�
cd apps/backend && pnpm run migration:run
```

###  ��h
```bash
# /�M� ��h (��3001)
cd apps/frontend && pnpm run dev

# /�� ��h (��3001APIM  /api/v1)
cd apps/backend && pnpm run start:dev

# �/�M� ((9�U)
pnpm run dev
```

### ����r
```bash
# ��M�
cd apps/frontend && pnpm run build

# ���
cd apps/backend && pnpm run build

# ��@	�(
pnpm run build

# ��q�
pnpm run build:packages
```

### pn��\
```bash
cd apps/backend

# ���
pnpm run migration:create

# �L��
pnpm run migration:run

# ����
pnpm run migration:revert
```

### �(�
```bash
# ESLint��
pnpm run lint

# Prettier<
pnpm run format

# TypeScript{���
pnpm run type-check
```

## ��Mn

### M﯃�� (.env.local)
```env
NEXT_PUBLIC_API_URL=http://localhost:3001/api/v1
NEXT_PUBLIC_APTOS_NETWORK=testnet
NEXT_PUBLIC_APTOS_API_KEY_TESNET=your_aptos_testnet_key
NEXT_PUBLIC_APTOS_API_KEY_DEVNET=your_aptos_devnet_key
```

### ﯃�� (.env)
```env
# pn�Mn
DB_HOST=localhost
DB_PORT=5432
DB_USERNAME=postgres
DB_PASSWORD=password
DB_NAME=cotrain

# RedisMn
REDIS_HOST=localhost
REDIS_PORT=6379
REDIS_PASSWORD=

# JWTMn
JWT_SECRET=your_jwt_secret
JWT_EXPIRES_IN=7d

# AptosMn
APTOS_PRIVATE_KEY=your_aptos_private_key
APTOS_NETWORK=testnet

# M�URL
FRONTEND_URL=http://localhost:3001
```

## API�c

�ЛSwagger API�c/�����
- **API�c**: http://localhost:3001/api/docs

## 8ß�!W

### 1. (7�����
- Aptos�ޥ���
- �/ (Petra, Martian, MSafeI)
- JWT Token�
- ��ޟ�

### 2. AI��
- P2PQ܂�Ѱ��
- ����ьO
- ��Z�!�e
- !.��0��*

### 3. :W��
- z����
- ��!.
��U
- �V��
- �
��h

### 4. ��ѧ���
- Q��Q��
- ��'�ѧ
- ��ۦ�*
- ����

### 5. V������
- !.����
- �V�M
- (���:6
- ��V���

##  ���y

### �h
- **�{(pnpm**: y�Mn��pnpm
- **�\z�**: (pnpm workspaces��V
- **H,�**: �pnpm-lock.yamlnݝV �'

### ReactH,|�'
- **(React 18.3.1**: React 19Aptos�MhX(|�'�
- **SSRQ**: ����(�7�2�
- **Hooks(**: u�React Hooks�M(a���-(

### HeroUI�
- **;�UI�**: HeroUI\:;�����
- **���**: (components/heroui/�U�HeroUI��
- **;�Mn**: �HeroUIMn���;�

### '�
- **�r**: (Next.js��e
- **�G**: (Next.js Image��
- **XVe**: RedisXAPI͔
- **Ҡ}**: '���(Ҡ}

### ՌK�
- ** ��w**: React DevTools + Next.js DevTools
- **APIK�**: (Swagger UIPostman
- **:W�K�**: (AptosK�Q
- **,0�**: (O�h ��w

## E��d

### 8��

1. **React Hook�**
   - n�(React 18.3.1
   - ����/&cn("use client"�
   - M(a���-(Hooks

2. **�ޥ�**
   - ��/&(�7���-(���
   - n��iU�Ō/(
   - �O�h�6���o

3. **���**
   - n�(pnpm�ŝV
   - ��TypeScript{��
   - .next�node_modules�UͰ��

4. **pn�ޥ�**
   - n�PostgreSQL�Redis�c(�L
   - �寃��Mn
   - �Docker�h�

5. **API(1%**
   - ����/&/�
   - n�API��Mn
   - �Q��B͔�

### �}�
```bash
# �Docker��
docker-compose ps

# ��(��
cd apps/frontend && pnpm run dev --debug
cd apps/backend && pnpm run start:dev --debug

# X
pnpm store prune
rm -rf node_modules .next
pnpm install
```

## !.W

1. **��<**: u�ESLint�PrettierMn
2. **Ф�o**: (�IФ�o
3. **{��h**: n�TypeScript{����
4. **K�**: :�������K�
5. **�c**: ���s�c���

---

d�c:Claude CodeЛy�
�n� ��-� �'�H�