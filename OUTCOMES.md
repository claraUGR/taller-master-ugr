# Exercise Outcomes Submission Template

**Student/Group Name**: Clara Liang Delgado Gómez 
**Level Completed**: newbie 
**Date**: 25/12/2025

---

## 📋 Exercise Summary

### Exercise: Fundamentals of Git: Commands, Branches & Remote Operations
**Status**: ✅ Completed 

**What I did**:

He completado todas las partes del nivel newbie. He aprendido a usar las SSH credential, además de algunos comando sbásicos de github que desconocía, ya que no he usado mucho gitHub

**Commands Used**:
```bash
# List the key Git commands you used across all parts of the exercise
Use git status #to see the untracked file
Use git add hello.txt #to stage the file
Use git commit -m "Add hello.txt with my name" #to commit
Use git log #to view your commit history
git branch feature/my-info #create a new branch
git checkout feature/my-info #change to that branch
git add my-info.txt #Commit your changes: add to Staging Area
git commit -m "Add personal information" #Commit your changes: Save the changes
git push origin feature/my-info #Push your branch to the remote repository:
git pull origin newbie # Pull the latest changes from remote:
git checkout main -- OUTCOME_TEMPLATE.md #Copy the outcome template:


```

**Results/Output**:
```

```

**Screenshots** (if applicable):
- [Screenshot 1: Description]
- [Screenshot 2: Description]

---

## 🎯 Key Learnings

**Main concepts I learned**:
1. [ "How to create and switch between branches efficiently"]
2. ["Configure SSH credentials"]
3. ["View commit history"]

**Skills I improved**:
- ["Reading and understanding Git logs"]
- ["Fundamental commands of Git]
- ["Remote Operations"]

---

## 🚧 Challenges Faced

### Challenge 1: [SSH Credentials]
**Problem**: [Describe the challenge you encountered]
No configuré las SSH credential desde el principio

**Solution**: [Explain how you resolved it or what you learned from it]
git remote set-url origin git@github.com:claraUGR/taller-master-ugr.git
**Commands/Approach**:
```bash
# Commands or approach used to solve the problem
ssh-keygen -t ed25519 -C "tu-email@ejemplo.com"
pbcopy < ~/.ssh/id_ed25519.pub
git remote set-url origin git@github.com:claraUGR/taller-master-ugr.git
```

---


## 💭 Personal Reflection

**What surprised me**:
[What unexpected things did you discover about Git?]
He usado anteriormente gitHub para compartir archivos y demás, pero no lo había usado nunca con comandos. Me ha sorprendido todo lo que se puede hacer

**What I found most difficult**:
[Which concepts or exercises were most challenging?]

El concepto de las ramas, creo que es bastante lioso ya que te puedes equivocar facilmente y puedes modificar el trabajo de tu compañero si no estás pendiente

**What I found most useful**:
[Which skills do you think will be most valuable in real projects?]
El uso fluido de todos los comandos de gitHbub, aunque no es algo inprescindible, pero puede aigerar mucho tu trabajo

**How I would apply this in real projects**:
[Describe how you might use these Git skills in professional work]
Para trabajar colabortivamente con compañeros si hay que tocar código a la vez y se está trabjando en el mismo proyecto a la vez
---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic | Confidence (1-5) | Notes |
|-------|------------------|-------|
| Basic Git commands | [2 ] ||
| Branching & merging | [ 1] | |
| Remote operations | [ 2] | |
| Conflict resolution | [1 ] | |
| History rewriting | [ 0] | |
| Git hooks | [ 0] | |
| Security practices | [0 ] | |

Tengo que practicar más
---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/miguel-oltra/taller-master-ugr/tree/group-X-outcomes/[level]`
- Key commits demonstrating your work:
  - Commit hash: [Short description]
  - Commit hash: [Short description]

**Additional files created** (if any):
- File 1: [Description]
- File 2: [Description]

---

## ✅ Completion Checklist

Before submitting, ensure you have:
- [ ] Completed the exercise for your chosen level (including all parts)
- [ ] Documented all commands used with their outputs
- [ ] Described challenges and how you resolved them
- [ ] Provided a thoughtful reflection on your learning
- [ ] Self-assessed your confidence in each topic
- [ ] Pushed your outcome branch to the remote repository
- [ ] Created a Pull Request (if required by your instructor)

---

## 📝 Additional Comments

gitHub es una herrmaienta muy completa pero a la vez compleja, por ello, para manejarte bien hay que prácticar bastante usando los diferentes comandos para coger soltura.

(base) clara@MacBook-Pro-de-Clara-2 taller-master-ugr % git status
On branch group-X-outcomes/newbie
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   OUTCOME_TEMPLATE.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        OUTCOMES.md



(base) clara@MacBook-Pro-de-Clara-2 taller-master-ugr % git branch -a 
  feature/my-info
* group-X-outcomes/newbie
  main
  newbie
  remotes/origin/HEAD -> origin/main
  remotes/origin/feature/my-info
  remotes/origin/intermediate
  remotes/origin/main
  remotes/origin/master
  remotes/origin/master-of-the-universe
  remotes/origin/newbie
(END)


(base) clara@MacBook-Pro-de-Clara-2 taller-master-ugr % git log --oneline --graph --all
* c7e2535 (origin/feature/my-info, feature/my-info) Add personal information
* 8d924ab (HEAD -> group-X-outcomes/newbie, newbie) Add hello.txt with my name
* 360f4a4 (origin/newbie) refactor: consolidate newbie exercises into single comprehensive exercise
* 5eedc97 docs: Add submission instructions to newbie level
* 45e1c31 Update README for newbie level exercises
| * 9602351 (origin/main, origin/HEAD, main) Adding GenAI guidelines
| * 7ad3af4 docs: update main branch files to reflect consolidated exercise structure (1 per l
evel)
| * 4d9131e chore: remove instructor files from repository tracking
| *   adbb307 Merge pull request #9 from miguel-oltra/patch-gitignore-update
| |\  
| | * e4709e6 Updated CODEOWNERS file
| | * 2a39a02 chore: add INSTRUCTOR_GUIDE.md to gitignore
| | * 0abdbae chore: add SUMMARY.md to gitignore for instructor files
| |/  
| * 88a54ab chore: Add .gitignore to exclude instructor files and sensitive data
| * e39ff08 PROMPT for updated
| * df1cfdd fix: Update CODEOWNERS to allow trainee work while protecting exercise branches
| * a011fad config: Add CODEOWNERS file for code review requirements
| * 769be64 docs: Add complete implementation summary
| * 9d008fa Updated README.MD with guidelines for the exercises
| * f66bf22 docs: Update MODEL_SPEC.MD with PROMPT 2 requirements
| * c24fd57 docs: Add outcome submission process and evaluation criteria
| * ec488d0 Update main README with complete training overview and navigation
|/  
| * b0fb9dc (origin/master-of-the-universe) refactor: consolidate master-of-the-universe exerc
ises into single comprehensive exercise
| * d1ef79f docs: Add submission instructions to master-of-the-universe level
| * 5bffa64 Update README for master-of-the-universe level exercises
|/  
| * b5d8eb6 (origin/master) refactor: consolidate master exercises into single comprehensive e
xercise on history rewriting
| * 960a0a6 docs: Add submission instructions to master level
| * f0055a0 Update README for master level exercises
|/  
| * 994450b (origin/intermediate) refactor: consolidate intermediate exercises into single com
prehensive exercise
| * a1c17e7 docs: Add submission instructions to intermediate level
| * 9f25f7a Update README for intermediate level exercises
|/  
* dc58203 Revert "Update README.md"
* e2db1ca (tag: v0.0.1) Update README.md
* 3d651c3 Update README.md
* 4cc5635 Initial commit
(END)
---

**Submission Date**: [Date]  
**Ready for Review**: ✅ Yes 
