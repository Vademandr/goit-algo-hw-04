# Sorting algorithms

Python has two built-in sorting functions: `sorted` and `sort`. Python's sorting functions use Timsort, a hybrid sorting algorithm that combines merge sort and insertion sort.

Compare three sorting algorithms: merge sort, insertion sort, and Timsort, in terms of execution time. The analysis should be supported by empirical data obtained by testing the algorithms on various data sets. Empirically verify the theoretical complexity estimates of the algorithms, for example, by sorting large arrays. Use the timeit module to measure the execution time of the algorithms.

Demonstrate that the combination of merge sort and insertion sort makes the Timsort algorithm much more efficient, and this is the reason why programmers, in most cases, use Python's built-in algorithms rather than coding their own. Draw conclusions.

## Таблиця результатів сортування різних алгоритмів

| Array Size       | Insertion Sort | Merge Sort | Timsort (Python's sorted) | Timsort (Python's sort) |
| ---------------- | -------------- | ---------- | ------------------------- | ----------------------- |
| Smallest (10)    | 0.000047600    | 0.00016620 | 0.00006780                | 0.00000699              |
| Small (100)      | 0.00228120     | 0.00266329 | 0.00007990                | 0.00007459              |
| Big (1,000)      | 0.32537739     | 0.03519660 | 0.001640799               | 0.00105399              |
| Largest (10,000) | 35.9752533     | 0.35069489 | 0.01610170                | 0.01542100              |

1. **Insertion Sort**: Сортування вставками показує дуже повільну продуктивність на великих масивах, що підтверджує його часова складність O($n^2$). Для малих масивів цей алгоритм може бути достатньо ефективним, але його використання на великих даних не рекомендується через значний час виконання.

2. **Merge Sort**: Сортування злиттям демонструє значно кращу продуктивність у порівнянні з сортуванням вставками на всіх розмірах масивів. Це узгоджується з його теоретичною складністю 
O(n logn). Навіть на великому масиві (10,000 елементів), час виконання залишається прийнятним.

3. **Timsort (sorted)**: Timsort, який використовується у функції sorted(), показує найкращі результати серед всіх алгоритмів. Час виконання залишається дуже малим навіть для великих масивів. Це підтверджує ефективність цього гібридного алгоритму, що поєднує сортування злиттям і сортування вставками.

4. **Timsort (sort)**: Результати аналогічні до Timsort (sorted), оскільки обидва використовують однаковий алгоритм. Це підтверджує стабільність та ефективність вбудованого алгоритму сортування в Python.

## Висновки:

**Insertion Sort** підходить для дуже малих масивів, але неефективний для
великих.

**Merge Sort** є стабільним і швидким для всіх розмірів масивів, особливо для
великих.

**Timsort (Python's sorted і sort)** демонструє найкращу продуктивність на всіх
розмірах масивів, будучи найшвидшим і найбільш ефективним алгоритмом для
загального використання.

Ці результати підкреслюють перевагу використання вбудованих алгоритмів
сортування Python (Timsort) для широкого спектра задач сортування завдяки їх
ефективності та оптимізації.
