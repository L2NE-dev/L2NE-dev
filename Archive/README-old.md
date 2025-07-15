# L2NE... (about me/us)

## 🌐 Frontend-side 🌐

I'm a passionate **Frontend Developer** with a strong focus on creating user-friendly web applications. I have experience working with modern technologies [Pug](https://pugjs.org/), [SCSS](https://sass-lang.com/), [TypeScript](https://www.typescriptlang.org/), along with HTML, CSS, and JavaScript (and also bigger frameworks). My goal is to deliver high-quality, responsive, and accessible interfaces that provide an exceptional user experience.

### 🛠️ Skills & Tools

- **Languages:** JavaScript/[TypeScript](https://www.typescriptlang.org/), HTML, CSS/[SCSS](https://sass-lang.com/)...
- **Tools:** **[Vite](https://vite.dev/)**, **[Git](https://git-scm.com/)**, pnpm/npm/yarn, other...
- **Frameworks:** **[Vanilla](https://vanilla-js.com/)**, **[Lit](https://lit.dev/)**, **[SolidJS](https://solidjs.com/)**, ***own conceptions***.
- **Assets:** **[Lucide](https://lucide.dev/)**, **['Source Sans'](https://fonts.google.com/specimen/Source+Sans+3)**, AI-Generated
- **Frameworks (in past):** Svelte, Vue, React
- **Other:**
  - Responsive Design
  - Accessibility (a11y)
  - Performance Optimization
  - Progressive Web Apps (PWA)
  - CSP, CORS, CORP, etc.
  - Backend (Node.js, Fastify, Vite)
- **Featured:**
  - Deep CSS/SCSS tricking
  - Passive CSS programming
  - Multi-level coding concept
  - Able to replicate most libraries
  - Able re-generate newer concepts
  - JS helping to CSS or vice versa

### 🧢 Some my tricks 🧢

#### 🌈 HSV? In my CSS?! 🌈

Yes, this is real HSV.

```scss
.hsv-based {
    --hsv-value: hsl(40 90 20); /* no-sense, it's hsv */

    // for string interpolation
    $L: calc((l / 100) * (1 - (s / 100) * 0.5));
    $S: calc(((l / 100) - #{$L}) / min(#{$L}, 1 - #{$L}));

    // use string interpolated $S and $L calc math
    background-color: hsl(from var(--hsv-value) h calc(#{$S} * 100) calc(#{$L} * 100));
}
```

#### 🔰 Addition for Evercookies... 🔰

> Code to block some actions from of naive users...

Why? Because after clear cache, memory process still remain
You can pass ban-system only if you block such events, or if you clear store in out of process

```js
//some process or memory still remains even after clearing storage...
addEventListener("beforeunload", saveToStorage);
addEventListener("pagehide", saveToStorage);

//
document.addEventListener("visibilitychange", (ev)=>{
    if (document.visibilityState === "hidden") {
        saveToStorage(ev);
    }
});

// but using such events may broke mechanism...
addEventListener("storage", (ev)=>{
    if (ev.storageArea == localStorage) {

    }
});
```

---

### 📑 License Agreements (Restrictions)

- Do not distribute without author mentions...
- Please, save something from original trademark.
- By making use of the Software for military purposes, you choose to make a 🐰 unhappy.

---

### 💓 Get In Touch

Feel free to reach out if you want to collaborate or just chat about tech!

- **Email:** <c24b@u2re.ru>
- **Telegram:** <https://t.me/u2re_space>
- **ETH/USDT:** `0x102E317665bBa4B4D2e2317Bf3c48F83FC13F4ec`
- **TRX/USDT:** `TCXePhsrVb63qymT84KP8cEfGWAb7qCKYJ`

---

### 🌈 Color Model spoiler

HSV? HSL? HWB? Someone else?... No, it's even more...

`t = H(t):F(x,y)`

Where:

- `t` variable RGB value...
- `H` hue value of `t`
- `F(x,y)` reversible and co-capable function, related to `H(t)`, which computes to origin `t` argument.

I don't know about creating math, color and conversion library idea.
