# UrbeLM

Plataforma RAG institucional, fork de InsightsLM (licencia MIT). Responsable: CIDETIU-URBE.

## Stack
- React + Vite + TypeScript
- Supabase + pgvector
- n8n (6 workflows), OpenRouter
- Despliegue on-premise con Cloudflare Tunnel (ya no VPS)

## Modelos (vía OpenRouter)
- Embeddings: `qwen/qwen3-embedding-8b`
- RAG: `deepseek/deepseek-chat-v3`
- Títulos: `gemini-2.5-flash`

## Restricción crítica
- La columna pgvector es de 1536 dimensiones. Confirmar compatibilidad con el modelo de embeddings ANTES de cargar documentos.

## Reglas para Claude
- Responde en español
- Respetar la licencia MIT del upstream
- Documentación en la serie CIDETIU de cuatro documentos
- Prosa sin rayas ni muletillas de IA

## Harness
- Lee `.claude/rules/aprendizajes.md` antes de cada tarea
- Tareas largas: contrato aprobado en `.claude/contracts/<tarea>.json` antes de escribir código
- Trabaja solo dentro de `.agent_worktrees/<tarea>` y solo en `escritura_permitida`
- Nunca te autoapruebes: un revisor distinto intenta romper el cambio
- Sin `.claude/receipts/recibo-<tarea>.json` con pruebas en 0 y veredicto APROBADO, no hay commit (el hook lo bloquea)
- Todo error corregido se agrega como regla a `.claude/rules/aprendizajes.md`

## Estado actual
- El repo solo contiene README y licencia; el código de la plataforma aún no se ha subido
- Kit de harness instalado: ver `.claude/HARNESS.md`
