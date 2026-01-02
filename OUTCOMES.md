# Exercise Outcomes Submission Template

**Student/Group Name**: Clara
**Level Completed**: master 
**Date**: 02/01/2026

---

## 📋 Exercise Summary

### Exercise: Rewriting History (Rebase and Amend Commits)
**Status**: ✅ Completed 

**What I did**:
He completado el nivel Master centrándome en la gestión avanzada del historial de Git. En la Parte 1, utilicé amend para corregir el último commit sin duplicarlo. En la Parte 2, realicé un rebase interactivo para limpiar el historial usando la función fixup para eliminar commits de "typos". En la Parte 3, realicé un rebase de una rama de característica sobre la rama master para lograr un historial lineal, evitando así los commits de merge innecesarios. Finalmente, documenté los riesgos de reescribir la historia pública.

**Commands Used**:
```bash
# List the key Git commands you used across all parts of the exercise
# Part 1: Amend
git commit --amend -m "Add complete configuration file"

# Part 2: Interactive Rebase
git rebase -i HEAD~3

# Part 3: Branch Rebase
git checkout -b feature/awesome-feature
git commit -m "Add awesome feature"
git checkout master
git commit -m "Update on master branch"
git checkout feature/awesome-feature
git rebase master

# Part 4: Verification
git log --graph --oneline --all -n 10
# etc.
```

**Results/Output**:
```
# Paste relevant command outputs, git log, or status messages
# Example:
$ git log --oneline -5
abc1234 feat: Add new feature
def5678 fix: Resolve merge conflict
```

**Screenshots** (if applicable):


---

## 🎯 Key Learnings

**Main concepts I learned**:
Reescritura de historia local: Cómo usar amend y rebase -i para limpiar el trabajo antes de compartirlo.

Historial lineal vs. No lineal: La diferencia visual y estructural entre integrar cambios con rebase (línea recta) frente a merge.

Seguridad en Git: La importancia de usar --force-with-lease para no sobrescribir el trabajo de otros.

**Skills I improved**:
Uso de editores en terminal: Navegación en Vim/Nano durante rebase interactivo.

Interpretación de logs: Uso de git log --graph para entender la estructura del repositorio.

Resolución de conflictos: Gestión de la base de una rama durante un rebase.

---

## 🚧 Challenges Faced

### Challenge 1: Navegación en el editor durante Rebase Interactivo

Problem: Al ejecutar git rebase -i, el terminal abrió Vim y no sabía cómo cambiar pick por fixup ni cómo guardar.

Solution: Aprendí los comandos básicos de Vim (i para insertar, Esc y :wq para guardar y salir).

**Commands/Approach**:
```bash
# Commands or approach used to solve the problem
```

---

### Challenge 2: [Brief title]
**Problem**: [Describe the challenge]

**Solution**: [Your resolution]

---

## 💭 Personal Reflection

Reescribir la historia con Git, mediante herramientas como rebase o amend, es una práctica esencial para mantener un repositorio profesional y legible. El rebase permite que las ramas de características se integren de forma lineal, evitando los "merge commits" innecesarios que a menudo ensucian el historial y dificultan el rastreo de cambios. Sin embargo, esta potencia conlleva un gran riesgo técnico y humano.

La regla de oro es nunca reescribir la historia de ramas públicas o compartidas. Si modificamos commits que otros compañeros ya han descargado (usando un push forzado), romperemos sus repositorios locales y crearemos conflictos difíciles de resolver, ya que los SHAs habrán cambiado. Por ello, el rebase interactivo debe reservarse exclusivamente para nuestra etapa de trabajo local.

En un entorno de equipo profesional, es vital usar git push --force-with-lease en lugar de --force. La opción force-with-lease es una medida de seguridad que solo permite subir cambios si nadie más ha actualizado la rama remota, evitando borrar accidentalmente el trabajo ajeno. En conclusión, mientras que el merge preserva la historia real tal cual sucedió con todas sus ramificaciones, el rebase nos permite diseñar una historia limpia, lógica y fácil de seguir para el futuro del proyecto, siempre que se haga con la precaución debida en ramas privadas.
---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic | Confidence (1-5) | Notes |
|-------|------------------|-------|
| Basic Git commands | [ 4] | |
| Branching & merging | [ 4] | |
| Remote operations | [ 4] | |
| Conflict resolution | [ 4] | |
| History rewriting | [ 4] | |
| Git hooks | [ 4] | |
| Security practices | [ 4] | |

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

**Submission Date**: [Date]  
**Ready for Review**: ✅ Yes / ❌ No
