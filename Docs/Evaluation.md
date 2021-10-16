이번 대회에의 평가 방식으로 Categorization Accuracy를 사용합니다. 얼마나 심한 사고가 발생했는가 4개의 클래스로 예측을 하고, 그것이 정답인지 아닌지로 점수를 구합니다.
아래 코드를 사용하여 계산할 수 있습니다.
```
from sklearn.metrics import accuracy_score
accuracy_score(y_pred, y_true)
```