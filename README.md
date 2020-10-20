# run this demo
## joint training
python run_sequence_labeling_and_text_classification_probability.py 
--task_name=snips 
--source_task_num=snip 
--do_train=true 
--do_eval=true 
--data_dir=D:/MachineLearningProjects/pythonProject/Demo/NLP/JointBert/snips_Slot_Filling/ 
--vocab_file=D:/MachineLearningProjects/pythonProject/Demo/NLP/JointBert/BERT-utilization/pretrained_model/uncased_L-12_H-768_A-12/vocab.txt 
--bert_config_file=D:/MachineLearningProjects/pythonProject/Demo/NLP/JointBert/BERT-utilization/pretrained_model/uncased_L-12_H-768_A-12/bert_config.json 
--init_checkpoint=D:/MachineLearningProjects/pythonProject/Demo/NLP/JointBert/BERT-utilization/pretrained_model/uncased_L-12_H-768_A-12/bert_model.ckpt 
--num_train_epochs=5.0 
--max_seq_length=32 
--train_batch_size=16 
--learning_rate=2e-5 
--output_dir=D:/MachineLearningProjects/pythonProject/Demo/NLP/JointBert/Demo-new/train/

## predicting
python run_sequence_labeling_and_text_classification_probability.py 
--task_name=snips 
--do_predict=true 
--data_dir=D:/MachineLearningProjects/pythonProject/Demo/NLP/JointBert/snips_Slot_Filling/  
--source_task_num=snip
--vocab_file=D:/MachineLearningProjects/pythonProject/Demo/NLP/JointBert/BERT-utilization/pretrained_model/uncased_L-12_H-768_A-12/vocab.txt 
--bert_config_file=D:/MachineLearningProjects/pythonProject/Demo/NLP/JointBert/BERT-utilization/pretrained_model/uncased_L-12_H-768_A-12/bert_config.json 
--init_checkpoint=D:/MachineLearningProjects/pythonProject/Demo/NLP/JointBert/Demo-new/train/model.ckpt-4088 
--max_seq_length=32 
--output_dir=D:/MachineLearningProjects/pythonProject/Demo/NLP/JointBert/Demo-new/predict/
