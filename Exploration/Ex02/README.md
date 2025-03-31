# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 김범모
- 리뷰어 : 김영숙


# PRT(Peer Review Template)
- [O]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - XGB, LGB 결과를 1:1로 혼합하여 private score 목표를 달성했습니다. 
    - XGB, LGB 에 대한 parameter를 random search로 조사했습니다
    ```bash
    
    def my_RandomSearch(model, train, y, param_dist, verbose=3):
    random_search = RandomizedSearchCV(
    estimator=model, 
    param_distributions=param_dist, 
    n_iter=5,  # 5번의 랜덤 검색
    scoring='neg_mean_squared_error',  # 정확도 기준
    cv=3,  # 3겹 교차검증
    verbose=verbose,
    random_state=random_state,
    n_jobs=-1
)
    
    # 모델 fitting
    random_search.fit(train, y)

    # 결과값 저장
    params = random_search.cv_results_['params']
    score = random_search.cv_results_['mean_test_score']
    
    # 데이터 프레임 생성
    results = pd.DataFrame(params)
    results['score'] = score
    
    # RMSE 값 계산 후 정렬
    results['RMSE'] = np.sqrt(-1 * results['score'])
    results = results.sort_values('RMSE')

    return results
    
    
    ```
        
    
- [O]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 함수내의 주석을 잘 추가하였습니다. 
    ````bash
    # 모델 2개 예측값의 평균을 최종 예측값으로 사용
xgb_pred = xgb_model.predict(x_test)
xgb_pred = np.expm1(xgb_pred)
lgb_pred = lgb_model.predict(x_test)
lgb_pred = np.expm1(lgb_pred)
average_pred = 0.5 * xgb_pred + 0.5*lgb_pred
print('xgb_rmse : ', np.sqrt(mean_squared_error(y_test, xgb_pred)))
print('lgb_rmse : ', np.sqrt(mean_squared_error(y_test, lgb_pred)))
print('average_rmse : ', np.sqrt(mean_squared_error(y_test, average_pred)))
    ```
        
- [O]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 알고리즘별로 성능 파라미터를 튜닝하여 사용했습니다.
    ```bash
        param_dist = {
    'learning_rate': [0.1, 0.5],
    'subsample':[0.7],
    'colsample_bytree':[0.7],
    'n_estimators': [500, 1000, 1500],  # 트리 개수
    'max_depth': [1, 10, 20],  # 트리 깊이
}
        ```
        
- [O]  **4. 회고를 잘 작성했나요?**
    - 실험 결과를 잘성했습니다. 
    ```bash
    # lgb는 n_estimators 하이퍼 파라미터는 별 영향 없는 거 같고 max_depth가 낮을 수록 안 좋음
    ```
        
- [O]  **5. 코드가 간결하고 효율적인가요?**
    - 함수화를 잘해서 사용했습니다. 


# 회고(참고 링크 및 코드 개선)
```
# 리뷰어의 회고를 작성합니다.
 - 램덤서치를 사용한것이 흥미롭고, xgb에 시간이 많이 걸린다는 것을 알려주셔서 도움이 되었습니다. 
 
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```

