# Run-to-Green Manual

1. Start PostgreSQL: `docker compose up -d`.
2. Install backend packages: `cd backend && npm install`.
3. Configure `.env` from `.env.example`.
4. Generate Prisma client: `npm run prisma:generate`.
5. Create migration: `npm run prisma:migrate -- --name init`.
6. Seed default rules and sample courses: `npm run seed`.
7. Start API: `npm run dev`.
8. Test fee calculator using a seeded course offering ID.
9. Start website advisor: `cd ../website && npm install && NEXT_PUBLIC_API_URL=http://localhost:4000 npm run dev`.
10. Start admin dashboard: `cd ../admin && npm install && npm run dev`.

## Data import plan
Use the prospectus as the golden source. Enter each school, course offering, exam body, tuition fee, practical fee, number of terms and tool requirements into seed files or admin forms.
