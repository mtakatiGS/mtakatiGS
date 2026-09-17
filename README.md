# Samwel G Mtakati - (<Compiler\\>)
**Backend engineer. I build systems that handle money, records, and the messy parts in between.**

Most of what I've built so far are learning projects rather than production systems with paying users — I'd rather say that up front than dress it up. What I do have is a habit of building something, finding out where the design was wrong, and understanding why. Below is the clearest example of that.

---

## Estate Management System

A property management system: units, tenants, leases, rent, arrears, maintenance requests, documents. Built to learn, not deployed to a real agency.

The hard part wasn't CRUD. It's that **a lease is a promise about the future and a payment is a fact from the past**, and the system has to store both and keep them agreeing with each other. Rent that is due doesn't exist yet. Rent that was paid can never change. I didn't see that distinction when I started.

So I did the obvious thing: I put a balance on the tenant and updated it whenever money came in. It works until someone asks a question about the past. Print a tenant's full payment history? Apply a late fee to an amount that went overdue in March? Reverse an entry that was keyed in wrong? Every one of those needs history the schema had already thrown away, because each payment overwrote the number instead of recording an event.

**The fix is a ledger.** Banks don't store your balance — they store an append-only list of transactions and add them up. A charge is a row. A payment is a row. A correction is a new opposing row, not a delete. The balance becomes something you derive and can prove, and the features that scared me stop being schema changes and become queries.

I haven't rebuilt it yet. When I do, that's the change.

`PHP` · `PostgreSQL` · relational modelling, auth, reporting

---

## Other projects

**Student Marks Management System** — assessments, grade validation, and reporting workflows. Interesting problem: validation rules are a business policy, not a constant, so they belong in data rather than hardcoded in the form.

**Security Guard Management System** — personnel, shift assignments, and site coverage. Essentially a scheduling problem wearing an admin panel, and scheduling is harder than it looks the moment two constraints conflict.

More in my repositories, including the unfinished ones.

---

## What I actually work on

Backend systems and APIs, relational data modelling, and the boring reliability work around them — auth, validation, tests, deployment. I'm most interested in the data model, because that's where the mistakes are expensive and where a bad decision quietly limits everything built on top of it.

Currently working on: designing schemas that record what happened instead of only what's true right now, and getting comfortable with Docker, CI, and deployment rather than treating "it runs locally" as done.

## Stack

**Languages:** `Python` ·  `C#` . `PHP` . `Kotlin` · `TypeScript`<br>
**Data:** `PostgreSQL` · `MySQL` · schema design<br>
**Web:** REST APIs · backend services · frontend when the project needs it<br>
**Tooling:** `Git` · `Linux` · `Docker` · `CI/CD`<br>

I'm not equally strong in all of these. Python and C# are where I'm most confident.

---

## Contact

Open to backend work, collaboration, and code review — especially the kind where someone tells me what I got wrong.

- Email — [mtakatigs@proton.me](mailto:mtakatigs@proton.me)
- WhatsApp — [+255 673 672 868](https://wa.me/255673672868)
- GitHub — [@mtakatiGS](https://github.com/mtakatiGS)
