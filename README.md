# AlumNet (Java / Spring Boot)

100% Java backend: Spring Boot + JDBC + PostgreSQL. The UI is the static page in
`src/main/resources/static/index.html`, served by the same Spring app, so there is one thing to deploy.
Tables and demo data are created automatically on first start.

## Run locally
Needs JDK 17+, Maven, and a Postgres database.
```bash
export DATABASE_URL="postgres://user:pass@localhost:5432/alumnet"
export SESSION_SECRET="any-long-random-string"
mvn spring-boot:run          # then open http://localhost:8080
```

## Deploy (Render + Neon, both free tiers)
1. Create a Postgres database at neon.tech and copy its connection string.
2. Push this folder to a GitHub repo.
3. On render.com: New > Web Service > pick the repo > Runtime: Docker.
4. Add environment variables: `DATABASE_URL` (the Neon string) and `SESSION_SECRET` (random string).
5. Deploy. Open the `onrender.com` URL. The first load after idle takes ~30 seconds on the free plan.

Demo logins: priya@nietstudent.in / student123, rahul@alumni.com / alumni123, admin@alumnet.com / admin123.
Change or delete them before sharing the link.
