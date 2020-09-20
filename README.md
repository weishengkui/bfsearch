# GridSearch
A Brute-Force based GridSearch Tool

Installation：
    pip install bfsearch

Usage:

```
from bfsearch import GridSearch

def score_func(a, b, **params):
    sc = a ** 2 + b ** 2 - 2 * a * b
    score_dict = {"score": sc, "info": "other info..."}
    return score_dict


if __name__ == '__main__':
    param_grid = {
        'a': range(10, 845),
        'b': range(4, 200)
    }
    g = GridSearch(score_func, param_grid)
    best_param, best_score_dict = g.run()
    print(best_param, best_score_dict)
```