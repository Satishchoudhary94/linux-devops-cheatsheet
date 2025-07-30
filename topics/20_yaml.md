# 📘 YAML Syntax Cheat Sheet

## ✅ Basic Structure

```yaml
name: Satish
active: true
count: 5
skills:
  - Linux
  - Docker
  - AWS
```

⚠️ Rules
Use 2 spaces for indentation (no tabs)

Key-Value pairs use :

Lists use -

Strings don't need quotes unless special characters are used

Booleans: true, false (lowercase)

Null: null or ~

🧪 Advanced Example

```bash
server:
  name: dev
  enabled: true
  ports:
    - 80
    - 443
  environment:
    DB_HOST: localhost
    DB_PORT: 3306


```
