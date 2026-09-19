# AI-Product-Review-Analyzer

- Overview:
    - This project represents what I have learned in the Hugging Face LLM Course.
    - This application takes a product review and determines the Sentiment(Positive / Negative), Topic of the review,
      the confidence of the model, and the generated summary, or short explanation of what the customer liked/disliked.

- Example Output:

    Sentiment: Positive
    Confidence: 91%

    Topics:
    • Product Quality
    • Shipping

    Summary:
    The customer is very satisfied with the headphones'
    sound quality and battery life but was unhappy with
    the slow shipping.

- Phases:

- Testing pretrained sentiment model using pipeline() API
      Output:         

        [{'label': 'POSITIVE', 'score': 0.9991727471351624}]
        [{'label': 'POSITIVE', 'score': 0.9938104748725891}]
        [{'label': 'POSITIVE', 'score': 0.9997978806495667}]
        [{'label': 'POSITIVE', 'score': 0.9998179078102112}]
        [{'label': 'POSITIVE', 'score': 0.9997859597206116}]

      Explanation: The output after training the pipeline() API sentiment model shows that for each of the 5 reviews,
                   each review is classified as having a POSITIVE sentiment and the model was able to classify each review                        with a 99% accuracy.
  - Fine-Tuning
        Output:

        TrainOutput(global_step=3, training_loss=0.4965078830718994, metrics={'train_runtime': 31.3992,
        'train_samples_per_second': 0.478, 'train_steps_per_second': 0.096, 'total_flos': 745129117440.0, 'train_loss':              0.4965078830718994, 'epoch': 3.0})

         Explanation: The output after training the Trainer model shows the evaluation after training the Trainer model                           over 3 epochs.

  - Evaluation
        Output:

        {'accuracy': 0.8, 'f1': 0.8888888888888888}

        Explanation: The output shows the accuracy and f1-score of the Trainer model after predicting sentiment from the                         test dataset.

    
