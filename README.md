# TestCaseGenerator
Project for automatical generating Test Cases

Description:
Имеется Объект тестирования.
Имеется тип тестируемого объекта, к которому можно добавить условия.
Условия могут быть вложенными и имеет 2 параметра (true/false):
  finished?
  exist_nested_conditions?

К каждому из условий задавать 2 вопроса:
  1. Условие окончательное?
  2. Имеются ли еще вложенные условия?

Объект: Операция закрытия депозитного продукта
Типы : BYN / USD / EUR
Условия:
  Последний день вклада                (1-false,2-true)
    Имеется возможность пролонгации      (1-false,2-true)
      В 5-ти дневный срок (1 день)         (1-true,2-false)
      В 5-ти дневный срок (3 день)         (1-true,2-false)
      В 5-ти дневный срок (5 день)         (1-true,2-false)
    Не имеется возможности пролонгации   (1-false,2-true)
      В 10-ти дневный срок (1 день)        (1-true,2-false)
      В 10-ти дневный срок (5 день)        (1-true,2-false)
      В 10-ти дневный срок (10 день)       (1-true,2-false)
  Не последний день вклада             (1-true,2-false)

КНОПКА "СГЕНЕРИРОВАТЬ ТЕСТ КЕЙС (открывающийся список - выбор уровня)"

MAX_LEVEL - из 1 объекта 3 типов и Условий: 1 уровень - 2 шт (1-false,2-true / 1-true,2-false)
                                            2 уровень - 2 шт (1-false,2-true / 1-false,2-true)
                                            3 уровень - 6 шт (1-true,2-false / 1-true,2-false / 1-true,2-false / 1-true,2-false / 1-true,2-false / 1-true,2-false)

BYN / Последний день вклада / Имеется возможность пролонгации / В 5-ти дневный срок (1 день)
BYN / Последний день вклада / Имеется возможность пролонгации / В 5-ти дневный срок (3 день)
BYN / Последний день вклада / Имеется возможность пролонгации / В 5-ти дневный срок (5 день)
BYN / Последний день вклада / Не имеется возможность пролонгации / В 5-ти дневный срок (1 день)
BYN / Последний день вклада / Не имеется возможность пролонгации / В 5-ти дневный срок (3 день)
BYN / Последний день вклада / Не имеется возможность пролонгации / В 5-ти дневный срок (5 день)
BYN / Не последний день вклада
USD / Последний день вклада / Имеется возможность пролонгации / В 5-ти дневный срок (1 день)
USD / Последний день вклада / Имеется возможность пролонгации / В 5-ти дневный срок (3 день)
USD / Последний день вклада / Имеется возможность пролонгации / В 5-ти дневный срок (5 день)
USD / Последний день вклада / Не имеется возможность пролонгации / В 5-ти дневный срок (1 день)
USD / Последний день вклада / Не имеется возможность пролонгации / В 5-ти дневный срок (3 день)
USD / Последний день вклада / Не имеется возможность пролонгации / В 5-ти дневный срок (5 день)
USD / Не последний день вклада
EUR / Последний день вклада / Имеется возможность пролонгации / В 5-ти дневный срок (1 день)
EUR / Последний день вклада / Имеется возможность пролонгации / В 5-ти дневный срок (3 день)
EUR / Последний день вклада / Имеется возможность пролонгации / В 5-ти дневный срок (5 день)
EUR / Последний день вклада / Не имеется возможность пролонгации / В 5-ти дневный срок (1 день)
EUR / Последний день вклада / Не имеется возможность пролонгации / В 5-ти дневный срок (3 день)
EUR / Последний день вклада / Не имеется возможность пролонгации / В 5-ти дневный срок (5 день)
EUR / Не последний день вклада

MIDDLE_LEVEL (Из вложенных последнего уровня оставить по одной. ):

MIN_LEVEL ()
