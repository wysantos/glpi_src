# Docker Container GLPI - Sources

## Estrutura:
```
.
├── LICENSE
├── offline
│   ├── Dockerfile
│   ├── glpi-9.1.3.tgz
│   └── glpi-start.sh
├── online
│   ├── Dockerfile
│   └── glpi-start.sh
└── README.md
```

# Criar a imagem:

```
cd online
docker build -t glpi .
```
