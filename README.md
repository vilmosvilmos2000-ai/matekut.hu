# matekut.hu

A **matekut.hu** hivatalos weboldala – matematika tanulás egyszerűen.

## GitHub Pages beállítás

A repository már elő van készítve a custom domainhoz.

### 1. GitHub Pages bekapcsolása (egyszeri)

1. Menj a repository **Settings → Pages** menüpontjába.
2. **Source**: Deploy from a branch  
   - Branch: `main`  
   - Folder: `/ (root)`
3. Kattints a **Save** gombra.
4. A **Custom domain** mezőbe írd be: `matekut.hu`
5. Pipáld be az **Enforce HTTPS** opciót (amint elérhető).

### 2. DNS beállítás (ez az egyetlen dolog, amit neked kell csinálnod)

A domain regisztrátorodnál (ahol a matekut.hu van) állítsd be a következő rekordokat:

#### Apex domain (matekut.hu) – A rekordok

| Típus | Host / Name | Value / Points to          | TTL  |
|-------|-------------|----------------------------|------|
| A     | @           | 185.199.108.153            | 3600 |
| A     | @           | 185.199.109.153            | 3600 |
| A     | @           | 185.199.110.153            | 3600 |
| A     | @           | 185.199.111.153            | 3600 |

#### www aldomain – CNAME (ajánlott)

| Típus | Host / Name | Value / Points to                    | TTL  |
|-------|-------------|--------------------------------------|------|
| CNAME | www         | vilmosvilmos2000-ai.github.io        | 3600 |

> **Megjegyzés:** Ha a regisztrátor támogat ALIAS / ANAME rekordot az apexhez, használhatod azt is:  
> `matekut.hu` → `vilmosvilmos2000-ai.github.io`

### 3. Ellenőrzés

- DNS propagáció után (néhány perc – 48 óra) a GitHub Pages felismeri a domaint.
- A site elérhető lesz: https://matekut.hu  és  https://www.matekut.hu

## Fejlesztés

- A főoldal: `index.html`
- Static site, Jekyll kikapcsolva (`.nojekyll`)
- Bármilyen további HTML/CSS/JS fájlt ide tehetsz, a `main` branchre pusholva automatikusan megjelenik.

---

Készítve a matekut.hu projekthez.
