# TORQUE evaluator

This repo hosts the evaluator for 
[TORQUE leaderboard](https://leaderboard.allenai.org/torque). (You can [read
about TORQUE on the AllenNLP website](https://allennlp.org/torque).)

This evaluator scores predictions provided in JSON format, and produces a file
with the scores in JSON format.

# Testing the evaluator

Run `test.sh` to build and test the evaluator.

The test will score the prediction file `predictions_small.json` against the
answers in `gold_small.json`. If everything is okay, then the test will pass.

(These gold and predictions JSON files are both representative of the real gold
and prediction files, but we put 3 QA pairs into them, thus the name "small".)

# Running the evaluator locally

You can follow the steps in test.sh to build and run the evaluator yourself
using Docker.

If you want to run the evaluator outside of Docker, look in the `evaluator`
directory and first install the dependencies specified in `requirements.txt`.
Then run `eval.py` as shown in the `test.sh` script.

# Submitting to the Leaderboard

The file `predictions_dummy.json` is a valid dummy submission file for the
[TORQUE leaderboard](https://leaderboard.allenai.org/torque). It contains
predictions for 4468 questions. If you submit it, you'll get get a dummy score
of XXX.

To submit your own predictions to the Leaderboard, produce a JSON file like
`predictions_dummy.json` with your predictions, and submit that.
