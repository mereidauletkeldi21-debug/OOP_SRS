# ATM Bank — C++ OOP Project

## Жоба туралы
Бұл жоба банкоматтың қарапайым жұмысын модельдейді: клиентті PIN арқылы тексеру, шот балансын көру, ақша салу және ақша шешу.

## Автор туралы мәлімет
- Аты-жөні: [аты-жөніңізді жазыңыз]
- Тобы: [тобыңызды жазыңыз]
- Нұсқа: 1 — ATM жүйесі

## Құрастыру
Барлық `.cpp` файлдарын бір командамен компиляциялауға болады:

```bash
g++ -std=c++17 -Wall -Wextra -pedantic main.cpp Client.cpp Account.cpp Transaction.cpp TransactionLog.cpp Bank.cpp ATM.cpp -o atm
```

Іске қосу:

```bash
./atm
```

Windows жүйесінде `atm.exe` файлын іске қосыңыз.

## Файлдар
- `Client.h/.cpp` — клиент және оның ішкі `Card` класы.
- `Account.h/.cpp` — банк шоты, баланс және статикалық шот санағышы.
- `Transaction.h/.cpp` — базалық транзакция және `Deposit`, `Withdrawal` туынды кластары.
- `TransactionLog.h/.cpp` — операциялар журналы.
- `Bank.h/.cpp` — клиенттер мен шоттарды басқару.
- `ATM.h/.cpp` — банкомат мәзірінің операциялары.
- `main.cpp` — бағдарламаны іске қосу.
- `UML.png` — класстар диаграммасы.

## Тапсырма талаптарының орындалуы
1. **Static members:** `Account::totalAccounts_`, `Transaction::transactionCount_` және статикалық әдістер.
2. **Friend:** `friend class Bank` және `friend` функция `printAccountDetails`.
3. **Nested class:** `Client::Card`.
4. **Object array:** `Bank` класындағы `Account accounts_[10]`.
5. **Composition:** `ATM` объектісінің құрамындағы `TransactionLog log_`.
6. **Aggregation:** `Bank` клиенттерді `Client*` көрсеткіштері арқылы байланыстырады; клиенттер банкке тәуелсіз жасалады.
7. **Inheritance:** `Transaction` базалық класы, `Deposit` және `Withdrawal` туынды кластары.
8. **Encapsulation:** деректердің көпшілігі `private`, оларға қатынау әдістер арқылы орындалады.

## Ескерту
Бұл оқу мақсатындағы демонстрациялық модель. Нақты банктік жүйеде PIN-ді сақтау, карта деректерін өңдеу, желілік қауіпсіздік және дерекқорға қосылу әлдеқайда күрделі болады.
