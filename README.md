## 

Tanto no Windows como no Linux, o build (contrução) e o run (execução) segue o mesmo comando:

- BUILD
```bash
docker build -t dockeragent:latest .
```

- RUN
```bash
docker run -e AZP_URL=<Azure DevOps instance> -e AZP_TOKEN=<PAT token> -e AZP_AGENT_NAME=mydockeragent dockeragent:latest
```
**OBS.:** Se você quiser um novo contêiner de agente para cada trabalho de pipeline, passe o **--once** sinalizador para o run comando.
```bash
docker run -e AZP_URL=<Azure DevOps instance> -e AZP_TOKEN=<PAT token> -e AZP_AGENT_NAME=mydockeragent dockeragent:latest --once
```