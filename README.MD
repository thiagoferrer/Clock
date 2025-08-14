# Conversor de Relógio (BRL ↔ US)

Este projeto em **Java** implementa um sistema de relógios capaz de trabalhar com dois formatos de horário:

* **BRLClock** → Formato brasileiro (24 horas)
* **USClock** → Formato americano (12 horas com AM/PM)

O sistema permite:

* Definir horas, minutos e segundos.
* Converter horários entre os dois formatos.
* Exibir o horário formatado.

---

## 🖥️ Exemplo de uso

```java
public class Main {
    public static void main(String[] args) {
        Clock brlClock = new BRLClock();
        brlClock.setSecond(0);
        brlClock.setMinute(0);
        brlClock.setHour(15);

        System.out.println(brlClock.getTime()); // 15:00:00

        System.out.println(new USClock().convert(brlClock).getTime()); // 03:00:00 PM
    }
}
```

---

## 📂 Estrutura do Código

* **Clock** → Classe abstrata (sealed) base para todos os relógios, contendo atributos e métodos comuns.
* **BRLClock** → Relógio brasileiro (formato 24h).
* **USClock** → Relógio americano (formato 12h com AM/PM).
* **Main** → Classe principal para executar o exemplo.

---

## 🔄 Conversão de horários

* **BRL → US:** Converte de formato 24h para 12h com indicador AM/PM.
* **US → BRL:** Converte de formato 12h AM/PM para 24h.

---

## 🛠️ Tecnologias

* **Java 17+** (utiliza `sealed classes` e `pattern matching` no `switch`)

---

## 📜 Licença

Este projeto está licenciado sob a licença MIT.

---
