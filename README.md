# Truthrail Starter

Create a private, durable Truthrail instance for your own AI assistant.

This repository is a **starter**, not the Truthrail Core source code. The public core lives at
`Dmitry-dev-pet/truthrail-core`.

## Start

1. Click **Use this template** → **Create a new repository**.
2. Create it as **Private**. `truthrail` is the recommended name.
3. Connect GitHub to your AI/chat client.
4. Give the AI write access only to the new private Truthrail repository. Your project
   repositories can remain read-only.
5. Send this:

```text
Use this repository as my private Truthrail instance.
Keep project repositories read-only unless I explicitly approve a narrower write capability.
Discover only the GitHub repositories in the scope I have approved.
Do not copy secret values.
Replace starter placeholders with my real GitHub owner and discovered state.
Ask me what I want to call my assistant, save that assistant profile, and attach the default Truthrail skill bundle.
Validate the instance and verify that a completely fresh chat can recover the same projects, assistant name, skills, and durable run state.
```

The default assistant skills are:

- `rebuild-context` — resume work from durable/live state;
- `recent-activity` — reconstruct what changed;
- `capability-route` — choose the narrowest safe execution route;
- `orchestrate-action` — execute an authorized action and verify the result separately.

`bootstrap-instance` is setup-only. `activate-capability` is optional and does not grant
permission by itself.

## Русский

1. Нажмите **Use this template** → **Create a new repository**.
2. Создайте **приватный** репозиторий, лучше с именем `truthrail`.
3. Подключите GitHub к чату.
4. Дайте AI write-доступ только к новому `truthrail`; проектные репозитории могут
   оставаться read-only.
5. Напишите:

```text
Используй этот репозиторий как мой приватный Truthrail.
Проектные репозитории оставляй read-only, пока я явно не разрешу конкретную write-capability.
Смотри только GitHub-репозитории в разрешённом мной scope.
Не копируй значения секретов.
Замени starter-placeholder'ы на моего GitHub owner и реально обнаруженное состояние.
Спроси, как я хочу назвать своего ассистента, сохрани его профиль и подключи стандартный набор навыков Truthrail.
Проверь instance и затем проверь из полностью нового чата, что восстанавливаются те же проекты, имя ассистента, навыки и durable run state.
```

## Security model

- assistant identity and skills do not grant permissions;
- no credential values belong in this repository;
- live GitHub/workflow/deployment/runtime state must be refreshed from authoritative systems;
- `executed` is not `verified`;
- write access is added later only for explicit capabilities that need it.

See Truthrail Core for the protocol and reference implementation.
