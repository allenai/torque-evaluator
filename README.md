# TORQUE-evaluator

This repo hosts the evaluator for [TORQUE](https://allennlp.org/torque.html). The gold json and prediction json are both in the correct format, but we only put 3 QA pairs into them (thus the name "small").

```
python eval.py --labels_file test_gold_small.json --preds_file test_preds_1e-5_7_small.json
```

The expected output should be
```
====Input Arguments====
{
  "labels_file": "test_gold_small.json",
  "metrics_output_file": "metrics.json",
  "preds_file": "test_preds_1e-5_7_small.json"
}
=======================
the current eval positive class Micro F1 (Agg) is: 0.8889
the current eval positive class Macro F1 (Relaxed) is: 0.6667
the current eval positive class Macro F1 (Agg) is: 0.6667
the current eval exact match ratio (Relaxed) is: 0.6667
2 Clusters
the current eval clustered EM (Agg) is: 0.5000
the current eval clustered EM (Relaxed) is: 0.5000
the current eval clusrered F1 (max>=0.8) is: 0.5000
```
