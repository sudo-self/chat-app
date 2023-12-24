# react-vite-supabase-0Auth-fullstack

PostgeSQL managed by [Supabase](https://supabase.io/)
[@supabase_io](https://twitter.com/supabase_io) (awsome real-time API).
 
- Front-end React + Vite
  
- Hosting [vercel](https://www.vercel.com/)

Build Node.js

npm install to setup


.env
VITE_SUPABASE_URL
VITE_SUPABASE_KEY

DB Table

| Field            | Type      |
| ---------------- | --------- |
| id               | BIGINT    |
| username         | VARCHAR   |
| text             | TEXT      |
| country          | VARCHAR   |
| is_authenticated | BOOLEAN   |
| timestamp        | timestamp |

SQL 

```sql
CREATE TABLE messages (
  id bigint GENERATED BY DEFAULT AS IDENTITY PRIMARY KEY,
  username VARCHAR NOT NULL,
  text TEXT NOT NULL,
  country VARCHAR,
  is_authenticated BOOLEAN DEFAULT FALSE,
  timestamp timestamp default now() NOT NULL
);
```

Supabase Enable Realtime

0Auth  callback URL: https://<project-ref>.supabase.co/auth/v1/callback

npm run dev

npm run build
