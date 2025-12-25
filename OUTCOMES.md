# Exercise Outcomes Submission Template

**Student/Group Name**: Clara 
**Level Completed**: intermediate
**Date**: 25/12/2025
---

## 📋 Exercise Summary

### Exercise: Merging, Conflict Resolution, and Tagging
**Status**: ✅ Completed 

**What I did**:
[Brief description of what you accomplished in this exercise. Since each level has one comprehensive exercise with multiple parts, describe your overall achievement and the key parts you completed.]

He aprendido a mergear ramas y resolver conflictos, lo de las etiquetas tengo que revisarlo, ya que no me ha quedado dle todo claro

**Commands Used**:
```bash
# List the key Git commands you used across all parts of the exercise

# etc.
# create 2 branches from intermediate 
git checkout intermediate
git checkout -b feature/header
git checkout intermediate
git checkout -b feature/footer
# create page and commit changes 
git add page.html
git commit -m "Add header to page"
# merge branches
git checkout intermediate
git merge feature/header
git merge feature/foote
#Create an annotated tag for your current work:
git tag -a v1.0 -m "First stable version with merged features"
#list all tag
git tag
# view tag inf
git show v1.0
#Push the tag to remote
git push origin v1.0
#Create a lightweight tag for testing:
git tag v1.0-test
#Create my Outcome Branch
git checkout intermediate
git checkout -b group-X-outcomes/intermediate
#get template
git checkout main -- OUTCOME_TEMPLATE.md

```

**Results/Output**:
```
(base) clara@MacBook-Pro-de-Clara-2 taller-master-ugr % git log --graph --oneline --all 
*   c47ea10 (HEAD -> group-X-outcomes/intermediate, tag: v1.0-test, tag: v1.0, intermediate) Merge footer with resolved conflicts
|\  
| * a9b2e84 (feature/footer) Add footer to page
* | 5aa97ff (feature/header) Add header to page1
* | aeabbb8 Add header to page
|/  
* 994450b (origin/intermediate) refactor: consolidate intermediate exercises into singl
e comprehensive exercise
* a1c17e7 docs: Add submission instructions to intermediate level
* 9f25f7a Update README for intermediate level exercises
| * eb63a93 (origin/group-X-outcomes/newbie, group-X-outcomes/newbie) Completar hello.t
xt
| * e0828d7 docs: Add newbie level exercise outcomes for Group X
| | * c7e2535 (origin/feature/my-info, feature/my-info) Add personal information
| |/  
| * 8d924ab (newbie) Add hello.txt with my name
| * 360f4a4 (origin/newbie) refactor: consolidate newbie exercises into single comprehe
nsive exercise
| * 5eedc97 docs: Add submission instructions to newbie level
| * 45e1c31 Update README for newbie level exercises
|/  
| * 9602351 (origin/main, origin/HEAD, main) Adding GenAI guidelines
| * 7ad3af4 docs: update main branch files to reflect consolidated exercise structure (
1 per level)
| * 4d9131e chore: remove instructor files from repository tracking
| *   adbb307 Merge pull request #9 from miguel-oltra/patch-gitignore-update
| |\  
| | * e4709e6 Updated CODEOWNERS file
| | * 2a39a02 chore: add INSTRUCTOR_GUIDE.md to gitignore
| | * 0abdbae chore: add SUMMARY.md to gitignore for instructor files
| |/  
| * 88a54ab chore: Add .gitignore to exclude instructor files and sensitive data
| * e39ff08 PROMPT for updated
| * df1cfdd fix: Update CODEOWNERS to allow trainee work while protecting exercise bran
ches
| * a011fad config: Add CODEOWNERS file for code review requirements
| * 769be64 docs: Add complete implementation summary
| * 9d008fa Updated README.MD with guidelines for the exercises
| * f66bf22 docs: Update MODEL_SPEC.MD with PROMPT 2 requirements
| * c24fd57 docs: Add outcome submission process and evaluation criteria
| * ec488d0 Update main README with complete training overview and navigation
|/  
| * b0fb9dc (origin/master-of-the-universe) refactor: consolidate master-of-the-univers
e exercises into single comprehensive exercise
| * d1ef79f docs: Add submission instructions to master-of-the-universe level
| * 5bffa64 Update README for master-of-the-universe level exercises
|/  
| * b5d8eb6 (origin/master) refactor: consolidate master exercises into single comprehe
nsive exercise on history rewriting
| * 960a0a6 docs: Add submission instructions to master level
| * f0055a0 Update README for master level exercises
|/  
* dc58203 Revert "Update README.md"
* e2db1ca (tag: v0.0.1) Update README.md
* 3d651c3 Update README.md
* 4cc5635 Initial commit
(END)
```

**Screenshots** (if applicable):
- [Screenshot 1: Description]
- [Screenshot 2: Description]

---

## 🎯 Key Learnings

**Main concepts I learned**:
1. ["How to merge branches"]
2. ["How to resolve conflicts"]
3. ["how to use tags"]

**Skills I improved**:
- ["Resolving merge conflicts"]

---

## 🚧 Challenges Faced

### Challenge 1: Merge conflicts
**Problem**: [Describe the challenge you encountered]
Aparecio problemas al realizar el merge

**Solution**: [Explain how you resolved it or what you learned from it]
Lo resolví manualmente sleccionado que se guardaran los cmabios d eambas ramas
**Commands/Approach**:
```bash
# Commands or approach used to solve the problem
```

---

## 💭 Personal Reflection

**What surprised me**:
[What unexpected things did you discover about Git?]
Que no lo soluciona automáticamente

**What I found most difficult**:
[Which concepts or exercises were most challenging?]
las etiquetas que no he podido comprenderlas dele tdo bien

**What I found most useful**:
[Which skills do you think will be most valuable in real projects?]
Aprender a mergear y solucinar conflictos

**How I would apply this in real projects**:
[Describe how you might use these Git skills in professional work]
mergenado código de varios desarrolladores, cuando cada uno trabaja en una parte del proyecto
---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic | Confidence (1-5) | Notes |
|-------|------------------|-------|
| Basic Git commands | [ 3] | |
| Branching & merging | [ 3] | |
| Remote operations | [3 ] | |
| Conflict resolution | [ 3] | |
| History rewriting | [0 ] | |
| Git hooks | [ 0] | |
| Security practices | [ 0] | |

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

[Any additional thoughts, questions, or feedback about the exercises]

---

**Submission Date**: 25/12/25
**Ready for Review**: ✅ Yes 
