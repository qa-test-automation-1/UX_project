# TaskFlow — User Flow

## Główny cel
Dodanie nowego zadania i powrót do listy zadań.

## Główny flow

```text
Dashboard
    ↓
Add Task
    ↓
Wpisanie nazwy zadania
    ↓
Save
    ↓
Task Added
    ↓
Dashboard
```

## Alternatywny flow

```text
Dashboard
    ↓
Wybór zadania
    ↓
Oznaczenie jako wykonane
    ↓
Dashboard
```

## Ekrany

### Dashboard
Lista aktualnych zadań oraz możliwość dodania nowego zadania.

### Add Task
Prosty formularz umożliwiający wpisanie nowego zadania.

### Task Added
Potwierdzenie, że zadanie zostało dodane.

## Główny scenariusz
Użytkownik uruchamia TaskFlow, dodaje zadanie, zapisuje je i wraca do Dashboardu, gdzie widzi nowe zadanie na liście.
