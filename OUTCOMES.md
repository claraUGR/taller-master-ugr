# Exercise Outcomes Submission Template

**Student/Group Name**: Clara
**Level Completed**:  master-of-the-universe
**Date**: 03-01-2026

---

## 📋 Exercise Summary

### Exercise: Branch Protection Rules and Security Best Practices
**Status**: ✅ Completed
**What I did**:

He implementado una estrategia de seguridad de nivel empresarial en el repositorio. Configuré reglas de protección de rama en `main` exigiendo Pull Requests, revisiones de Code Owners y, lo más importante, commits firmados digitalmente. Generé una llave GPG RSA de 4096 bits vinculada a mi identidad institucional, sincronicé mi entorno local de Git para la firma automática y realicé auditorías de seguridad buscando secretos filtrados y configurando un archivo `.gitignore` robusto.

**Commands Used**:
```bash
# List the key Git commands you used across all parts of the exercise
# Generación de llaves y configuración
gpg --full-generate-key
gpg --list-secret-keys --keyid-format=long
gpg --armor --export 5954874F08637416

# Configuración de Git
git config --global user.signingkey 5954874F08637416
git config --global user.email "e.cdelgom@ms.ugr.es"
git config --global commit.gpgsign true

# Verificación y corrección
git log --show-signature -1
git commit --amend --no-edit --reset-author -S

# Seguridad
git log -p | grep -i "password\|api_key\|secret\|token" | head -20
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
- [Screenshot 1: Description]
- [Screenshot 2: Description]

---

## 🎯 Key Learnings

**Main concepts I learned**:
Criptografía Asimétrica en Git: Entender cómo el par de llaves pública/privada asegura la autoría de un commit.

Gobernanza de Repositorios: Configuración de reglas que impiden que incluso los administradores suban código sin revisión.

Gestión de Identidad: La importancia de la coincidencia exacta de correos electrónicos entre GPG, Git local y perfiles de GitHub.

**Skills I improved**:
Troubleshooting de GPG: Resolución de errores de terminal (entropy/TTY) y de validación de firmas.

Auditoría de seguridad: Uso de expresiones regulares para escanear fugas de secretos en el historial de Git.

Administración avanzada de GitHub: Configuración de Branch Protection Rules.

---

## 🚧 Challenges Faced


### Challenge 1: Error "Screen or window too small"

Problem: Al intentar generar la llave GPG, el agente de pinentry fallaba porque la ventana de la terminal no cumplía con los requisitos de tamaño para la interfaz.

Solution: Se solucionó exportando la variable TTY y maximizando la ventana de la terminal para permitir la interfaz visual de entrada de contraseña.

export GPG_TTY=$(tty)
gpg --full-generate-key


**Commands/Approach**:
```bash
# Commands or approach used to solve the problem
export GPG_TTY=$(tty)
gpg --full-generate-key
```

---

### Challenge 2: Badge "Unverified" en commits firmados

Problem: A pesar de firmar los commits, GitHub los marcaba como no verificados. El problema era una discrepancia entre el email de la llave (go.ugr.es) y el email configurado en Git y verificado en GitHub (ms.ugr.es).

Solution: Se generó una nueva llave vinculada al email correcto, se configuró user.email en Git y se realizó un --amend de los commits para refirmarlos con la identidad correcta

---

## 💭 Personal Reflection

La implementación de firmas GPG y reglas de protección de ramas representa un salto cualitativo desde el desarrollo personal hacia la ingeniería de software profesional. En entornos corporativos, donde el código puede manejar activos financieros o datos personales sensibles, la identidad del desarrollador no puede dejarse al azar. Sin firmas GPG, cualquier usuario con acceso al repositorio podría suplantar la identidad de otro configurando simplemente el nombre y correo en su Git local; la verificación digital rompe esta vulnerabilidad, garantizando el no repudio: si un commit está firmado, tenemos la certeza técnica de que proviene del dueño de la llave privada.

Por otro lado, la gobernanza mediante Branch Protection Rules es fundamental para mantener la integridad del flujo de trabajo (CI/CD). Al exigir revisiones obligatorias y estados de comprobación aprobados, eliminamos el factor de "error humano" único. Un desarrollador senior o "Master of the Universe" debe entender que estas restricciones no son obstáculos a la productividad, sino salvaguardas que protegen la estabilidad del producto final.

Finalmente, la gestión proactiva de datos sensibles mediante herramientas de escaneo y archivos .gitignore adecuados demuestra un "Security-first mindset". En mi experiencia durante este taller, aprendí que la seguridad no es un parche que se aplica al final, sino una práctica constante que comienza desde la generación del primer bit de una llave criptográfica. La capacidad de auditar el historial de Git en busca de secretos es una habilidad crítica en un mundo donde una sola API Key filtrada puede comprometer toda una infraestructura en la nube. Este ejercicio me ha proporcionado las herramientas necesarias para liderar proyectos con estándares de seguridad industriales.

---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic | Confidence (1-5) | Notes |
|-------|------------------|-------|
| Basic Git commands | [5 ] | |
| Branching & merging | [5 ] | |
| Remote operations | [ 5] | |
| Conflict resolution | [5 ] | |
| History rewriting | [ 5] | |
| Git hooks | [ 5] | |
| Security practices | [5 ] | |

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
