# Day 1: Linux User Setup with Non-Interactive Shell

## 1 - To accommodate the backup agent tool's specifications, the system admin team at xFusionCorp Industries requires the creation of a user with a non-interactive shell. Here's your task:
## 2 - Create a user named jim with a non-interactive shell on App Server 1.

# Solución: 

## 🧑‍💻 1. Conéctate al servidor
### Primero entra al servidor (normalmente por SSH): 
```
ssh tony@stapp01
```
## ⚙️ 2. Crea el usuario con shell no interactivo
### Usa este comando: 
```
sudo useradd -s /sbin/nologin jim
```
# 🔍 Luego verifica
```
grep jim /etc/passwd
```

# 📌 Explicación:
# crea el usuario
```
useradd
```
# asigna un shell no interactivo (no podrá iniciar sesión) 
```
-s /sbin/nologin: 
```
# 🔍 3. Verifica que se creó correctamente : 
```
grep jim /etc/passwd
```
# Deberías ver algo como: 
```
jim:x:1001:1001::/home/jim:/sbin/nologin
```
