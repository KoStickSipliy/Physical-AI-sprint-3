# own_experiment

- Итераций: 1001; сред: 2048; seed: 1; обучение с нуля.
- Финальный mean_reward: 940.23; время обучения: 1209 с.
- Последний чекпоинт: `model_1000.pt`. Промежуточные чекпоинты в пакет не включены.
- SR не измерен: лимит Colab.
- Исходный TensorBoard-файл сохранён без изменений.

`train.ipynb` — компактная копия обучения; `training.txt` — весь доступный вывод обучения из исходного ноутбука; `training_metrics.csv` — метрики сохранённых итераций (793–1000, 208 строк); `experiment.json` — настройки опыта; `config.json` — PPO; `evaluation.json` — статус оценки. Colab обрезал ранний текстовый вывод.

Команда инференса из корня этого пакета в подготовленной Linux/Colab-среде:

```bash
MUJOCO_GL=egl python src/inference.py --checkpoint experiments/own_experiment/model_1000.pt --episodes 10 --seed 42 --record experiments/own_experiment/evaluation.mp4
```

Исходные ноутбуки всех пяти запусков при инференсе загружали baseline. Неверно отнесённые к этому опыту выводы в эту копию не перенесены. Исходные файлы пользователя оставлены без изменений.
