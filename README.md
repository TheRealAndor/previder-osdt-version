# previder-osdt-version

Publiek versiebestand voor de Previder OS Deployment Tool.
De tool zelf staat in privé-repo's; dit bestand bevat bewust alleen versienummers.

De tool leest bij het opstarten:

`https://raw.githubusercontent.com/TheRealAndor/previder-osdt-version/main/version.json`

## Formaat

Eén sleutel per architectuur. Een tool kijkt alleen naar zijn eigen sleutel.

```json
{
  "x64":   { "version": "1.6", "released": "2026-10-21" },
  "arm64": { "version": "1.0", "released": "2026-11-01" }
}
```

- `version`: `Major.Minor` of `Major.Minor.Build`, vergeleken als `[version]`.
- Een ontbrekende sleutel betekent: geen update-melding voor die architectuur.

## Bijwerken

Pas bijwerken **nadat** de nieuwe stick/boot.wim beschikbaar is. GitHub cachet raw-bestanden een paar minuten, dus een wijziging is niet direct overal zichtbaar.
