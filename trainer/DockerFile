FROM tensorflow/tensorflow:1.5.1
ADD task.py /root/tf-trainer/task.py
ADD model.py /root/tf-trainer/model.py
ADD training_data /root/tf-trainer/trainig_data
RUN mkdir /root/tf-trainer/results
ENTRYPOINT python /root/tf-trainer/task.py --train-files $TRAIN_FILE --eval-files $EVAL_FILE --job-dir $RESULTS_DIR --train-steps $TRAIN_STEPS --eval-steps $EVAL_STEPS --num-epochs $NUM_EPOCHS
