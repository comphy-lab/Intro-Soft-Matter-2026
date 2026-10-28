# Introduction to Soft Matter 2026

The coding assessment for the 2026 run of *Soft Condensed Matter: An Introduction* (Durham University). Each student chooses one of two singularities, codes it, submits the work here as a pull request, and presents and defends it in the final session.

**Repository**: [https://github.com/comphy-lab/Intro-Soft-Matter-2026](https://github.com/comphy-lab/Intro-Soft-Matter-2026)
**Course notes**: [https://blogs.comphy-lab.org/Lecture-Notes/Intro-Soft-Matter/2026/0-README](https://blogs.comphy-lab.org/Lecture-Notes/Intro-Soft-Matter/2026/0-README)

| Part | Weight |
|---|---|
| Pull request (code, figures, README, AI log) | 40% |
| Presentation and defence in the final session | 60% |

## Dates (Wednesdays, 2026)

| Date | Step |
|---|---|
| 18 November | choose Option A or Option B |
| 2 December | open your pull request |
| 2–9 December | written feedback on your pull request |
| 9 December | present and defend your work in the final session |

---

## The questions

Every singularity in the course is examined with the same four questions:

1. **Singular?** Which quantity goes to zero, or diverges, and where or when?
2. **Self-similar?** Do rescaled profiles collapse onto one curve?
3. **Universal?** What does the local solution forget about the initial or far-field conditions?
4. **Regularised?** Which physics, absent from the equation, stops the divergence?

Each option asks a subset of them. Answer them with evidence from your own computations.

## Option A: a moving contact line

A liquid wedge moves steadily over a solid. In the frame of the contact line, the film thickness $h(x)$ at distance $x$ from the line obeys the lubrication equation

$$\frac{d^3h}{dx^3} = -\frac{0.01}{h^2},$$

with

- $h(0) = 0$ (the film ends at the contact line),
- $h'(0) = 1$ (unit slope at the contact line),
- $h''(\infty) = 0$ (the curvature dies out far away).

The constant $0.01$ measures the speed of the line relative to surface tension.

**Questions**: Is the problem singular? How is it regularised? Is the result universal?

## Option B: a rupturing film

A thin liquid film on a solid is thinned by van der Waals attraction. In dimensionless form, its thickness $h(x,t)$ obeys

$$h_t + \left(h^3 h_{xxx}\right)_x + \left(\frac{h_x}{h}\right)_x = 0,$$

on a periodic domain, starting from

$$h(x,0) = 1 + \varepsilon \cos kx.$$

**Questions**: Is the flat film unstable? Is the rupture singular? Is it self-similar? Is it universal?

---

## What to submit

Put every file directly in `submissions/`, with your exact GitHub username and an underscore as a prefix: `submissions/<github-user>_<filename>`. GitHub user `octocat` would submit, for example:

| File | Content |
|---|---|
| `submissions/octocat_contact-line.py` | your code, in any language (one or more files) |
| `submissions/octocat_slope.png` | the figures you discuss (any number) |
| `submissions/octocat_README.md` | the problem, your approach, your answers to the questions for your option, and how to run your code |
| `submissions/octocat_AI-log.md` | the prompts you used, what you checked, and what you changed |

An automated check verifies the location, the filename prefix, and that the README and the AI log are present. It does **not** run submitted programs. Your code is read and run by the instructor during feedback.

## AI is encouraged

Use any AI tool for any part of the work. Keep the log as you go: what you asked, what came back, how you tested it, and what you changed. In the final session you must be able to explain every line of your code and every figure you show; the defence is about your understanding, whoever typed the code.

## The final session

Each presentation covers the problem, how you approached it (including the checks that make you trust your numbers), what you found for each question, and then a defence: any line of code or any figure can be questioned. Plan for about 5 minutes plus 3 minutes of questions; the exact timing depends on the size of the class.

---

## Public visibility and consent

This is a public repository. Your files, commit history, GitHub username, pull request description and discussion will be publicly visible and may remain in the repository history. Do not include student numbers, marks, private contact details, API keys, passwords, tokens or other sensitive information. By opening a pull request you confirm that you understand this public submission route and consent to publishing the material you submit. If you do not want to submit publicly, contact the course instructor for an alternative before opening a pull request.

## How to submit

### In the browser

1. Open [https://github.com/comphy-lab/Intro-Soft-Matter-2026](https://github.com/comphy-lab/Intro-Soft-Matter-2026) and click **Fork**.
2. In your fork, open the `submissions` folder and choose **Add file** → **Upload files**.
3. Upload your files, already named with your GitHub username prefix, and check that GitHub shows them under `submissions/`.
4. Write a commit message that says what you added, for example `Add Option B rupture solver, figures, README and AI log`.
5. Click **Contribute** → **Open pull request** and fill in the template.

### From a terminal

```bash
# Fork on GitHub first, then:
git clone https://github.com/YOUR-USERNAME/Intro-Soft-Matter-2026.git
cd Intro-Soft-Matter-2026
git checkout -b submission-YOUR-USERNAME

cp /path/to/solver.py submissions/YOUR-USERNAME_solver.py
cp /path/to/README.md submissions/YOUR-USERNAME_README.md
cp /path/to/AI-log.md submissions/YOUR-USERNAME_AI-log.md
git add submissions/YOUR-USERNAME_*
git commit -m "Add Option A contact-line solver, README and AI log"
git push origin submission-YOUR-USERNAME
```

Then open the pull request on GitHub. You can keep pushing commits to the same branch until the deadline; the pull request updates itself.

## Reading

- J. Eggers and M. A. Fontelos, *Singularities: Formation, Structure, and Propagation*, Cambridge University Press (2015). Chapters 1–3 for the framework; §15.2 for contact lines.
- J. H. Snoeijer and B. Andreotti, Moving contact lines: scales, regimes, and dynamical transitions, *Annu. Rev. Fluid Mech.* **45**, 269–292 (2013).
- A. Oron, S. H. Davis and S. G. Bankoff, Long-scale evolution of thin liquid films, *Rev. Mod. Phys.* **69**, 931–980 (1997).
- V. Sanjay, Singularities in soft matter systems, *Contemporary Physics* (2026), [doi:10.1080/00107514.2026.2721118](https://doi.org/10.1080/00107514.2026.2721118); [arXiv:2608.11060](https://arxiv.org/abs/2608.11060).

## Questions?

Open an issue in this repository or ask in class.

## Licence

GPL-3.0; see [LICENSE](LICENSE).
