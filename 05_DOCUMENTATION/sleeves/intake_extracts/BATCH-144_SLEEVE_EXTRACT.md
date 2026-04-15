# BATCH-144 — Sleeve Extract

## Scope
Sleeve identity and resleeving signals extracted from the builder source.

## Persona Switching Signal
The source treats persona switching as a runtime mechanism.
It is defined through fields or ideas such as:
- `multi_persona_mode_enabled`
- `persona_switch_trigger_method`

## Resleeving Implications
Persona switching behaves like runtime resleeving.
The source also raises memory-model decisions:
- shared memory
- isolated memory

These decisions affect identity continuity and state persistence.

## Temporary Override Signal
Instruction injection acts as a temporary sleeve override mechanism through:
- temporary scope
- priority policy
- revert-to-base trigger

## Sleeve-Level Doctrine Signal
- base persona remains a stable identity layer
- temporary injection can override or append behavior
- persona switching changes sleeve state
- memory-sharing policy determines continuity boundaries
