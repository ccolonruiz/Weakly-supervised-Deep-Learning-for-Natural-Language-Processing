# Weakly Supervised Deep Learning for Natural Language Processing.

Artificial intelligence (AI) has proven to be a cross-cutting tool that helps to perform tasks
typically performed by humans automatically. In particular, supervised approach algorithms have
achieved great success in learning implicit patterns in data and extracting information by learning
from annotated training datasets consisting of tuples of two elements: a feature vector
describing an example and a label or set of labels indicating the desired output of the model to
be trained given that particular example.

In Machine Learning, models are trained with features defined by researchers and experts to
provide relevant information about each example for a given task, resulting in a resourceintensive and time-consuming task. On the other hand, deep learning algorithms can learn these
features themselves from the raw data, outperforming traditional machine learning algorithms
but at the cost of being data-hungry algorithms that require large annotated datasets and, in
many tasks, such sets can be difficult to obtain, not being sufficient in quantity or quality due to
the high cost of labeling the data or due to their nature.

The increasing availability of Electronic Health Records (EHR) and patient reviews has resulted in
a large volume of clinical documents where some information is unstructured. Due to the high
cost of time and resources to extract information from clinical texts, there has been increasing
interest in research and development of Natural Language Processing (NLP) techniques to
automate the process and optimize research into new clinical solutions and approaches to
improve patient results. However, clinical documents present additional challenges compared to
generic texts due to the difference in the language features used, specific acronyms, and nonstandardized jargon by each system or clinical center. In addition, the need to de-identify and
anonymize texts to ensure data privacy limits access to clinical documents, resulting in a scarcity
of annotated corpora.

This Ph.D. thesis's main hypothesis is that applying transfer learning mechanisms with semisupervised approaches and pre-trained generative language models, which provide synthetic
instances or synthetic feature representations, could improve model performance in situations
where a scarce volume of annotated data is available. Furthermore, fine-tuning models in similar
tasks with an analogous text distribution could increase model performance in such data-limited
scenarios. To test this hypothesis, the main objective is to investigate, design, and evaluate the
performance of different models for Sentiment Analysis (SA) in drug reviews and Named Entity
Recognition (NER) in medical prescriptions, using supervised and weakly supervised approaches.

The results show that pre-trained large language models like Bidirectional Encoder
Representations from Transformers (BERT) outperform traditional deep learning models such as
Convolutional Neural Networks (CNN) and Recurrent Neural Networks (RNN). Pre-training
language models on unannotated corpora from similar domains can help improve their
performance on specific tasks through transfer learning when limited annotated data is available.
However, this depends on the model capabilities of language understanding and the amount of
annotated data available. Furthermore, there are limitations to generalizing when the linguistic
features between pre-training and task-specific corpora are heterogeneous.

In low annotated data scenarios for SA in drug reviews, the use of generative adversarial
networks in a semi-supervised (SSGAN) setting is proposed. We compare the performance of
BERT-based models in the SSGAN approach fine-tuned with a few labeled data and the rest as
unlabelled data, with a baseline fine-tuning of BERT-based models on labeled data only. The
SSGAN approach employs labeled and unlabeled data to learn to generate synthetic
representations similar to those of the original texts provided by BERT. These synthetic
representations attempt to fool the model's discriminator, forcing BERT to improve the original
text representations, thus aiding the SA task. The results show that, although this approach can
help pre-trained models identify underrepresented examples, it is far from mitigating the lack of
annotated data. Despite the promising results, further research on generating synthetic text
representations in an SSGAN approach is needed.

Furthermore, it is proposed to fine-tune Generative Pre-trained Transformers (GPT) to the
available labeled data to increase the training set of discriminative models with new synthetic
reviews. We compare the performance of BERT-based models that are fine-tuned to the original
dataset and the augmented dataset with the synthetic reviews. The results indicate that pretrained generative models such as GPT are able to generate synthetic texts consistent with
linguistic patterns not present in the original training set, helping discriminative models mitigate
the lack of annotated data. However, it is important to note that fine-tuning pre-trained
generative models to an unbalanced dataset negatively affects the generation of
underrepresented class data.

In low annotated data scenarios for NER in medical prescriptions, it is proposed a prior finetuning of BERT-based models to annotated corpora in similar tasks. The results show that this
procedure helps in the subsequent fine-tuning to mitigate the lack of annotated data in the
target task by transferring learning. However, the difference in the distribution of texts may limit
generalisability in specific contexts.

To summarise, the results show that, although there is room for improvement, the proposed
approaches help to mitigate the lack of annotated data, thus supporting the hypothesis of the
Ph.D. thesis.

This thesis contributes to exploring different approaches to mitigate the weak performance of
deep learning models due to the lack of annotated data for SA and NER tasks. It provides a
detailed review of related work in the literature, an in-depth description of the approaches
employed, and a comprehensive discussion and comparison of the results obtained.
Furthermore, the study of the proposed systems constitutes a baseline for future research work
on PLN tasks in the clinical setting and can be implemented as a medical resource.
