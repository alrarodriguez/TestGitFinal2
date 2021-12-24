# TestGitFinal2

Pasos para crear el repositorio de código simple con el flujo de trabajo especificado.

git init
git remote add origin https://github.com/alrarodriguez/testgitfinal.git
git remote -v
git status
git add .
git commit -a -m "First Change"
git push origin master
git tag v1.0.0
git push origin v1.0.0


git checkout -b hotfix
git status
git add .
git commit -a -m "Second Change"
git push origin hotfix
git checkout master
git merge --no-ff hotfix -m "Merger Branch Hotfix"
git push origin master
git tag v1.0.1
git push origin v1.0.1


git checkout -b feature1
git status
git add .
git commit -a -m "Third Change"
git push origin feature1
git checkout master


git checkout -b feature2
git status
git add .
git commit -a -m "Third Change 2"
git push origin feature2


git checkout master
git merge --no-ff feature1 -m "Merge Branch Feature1"
git push origin master
git tag v1.1.0
git push origin v1.1.0

git checkout feature2
git status
git add .
git commit -a -m "Third Change 3"
git push origin feature2
git checkout master


git merge --no-ff feature2 -m "Merge Branch Feature2"
(Conflicto - Comparar y escoger cambios)
git add .
git commit -a
git push origin master
git tag v1.2.0
git push origin v1.2.0
