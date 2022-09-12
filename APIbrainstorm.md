# API Response Objects

## Defintionen

---

### User

- Account Data
```json
{
  "_id": "string",
  "name": "string",
  "birthdate": "Date",
  "sex": "string",
  "plans": "Trainingsplan[]",
}
```

- Body Definition
```json
{
  "height": "string",
  "weight": "string",
}
```

### Pläne

- Trainingsplan
```json
{
  "name": "string",
  "split": "number",
  "trainingsTage": "Trainingstag[]",
  "nextDay": "number",
}
```

- Trainingstag
```json
{
  "_id": "string",
  "name": "string",
  "uebungen": [{
    "exercise": "exercise",
    "sets": "int",
    "reps": "int",
  }],
  "historyData": "Trainingseinheit",
}
```

- Trainingseinheit
```json
{
  "trainingstagId": "string",
  "date": "Date",
  "exercises": "Übungseinheit[]",
}
```

- Übungseinheit
```json
{
  "exerciseId": "string",
  "date": "Date", 
  "notes": "string[]",
  "sets": [{
    "type": "warmup | working | backoff",
    "weight": "number",
    "reps": "number",
    "10RM": "number",
  }],
}
```

- Übung
```json
{
  "name": "string",
  "description": "string",
  "gifURL": "string",
  "muskel": "string/Enum",
  "equipment": "string",
}
```

- Last Week Trainings
```json
{
  [{
    "date": "Date",
    "trained": "boolean",
  }],
}
```

