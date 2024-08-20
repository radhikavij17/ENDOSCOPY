# ENDOSCOPY
Start with the preprocessing file and mount the doc to google drive. Once the pickled batches of extracted frames with their corresponding label from the csv files are loaded, you do not need to do that again.

Then do the train test split - depending on if you want to do all the labels or labels with 'other' removed.

After the train test split run the sequence generator with the corresponding data (ie all labels or with 'other' removed)

After that you can use the models. You can run more than one model in a single runtime after loading the train test split but maybe change the names of the model so that the cells dont get confused between models. Also bear in mind that the models can sometimes take several hours to load. 

The GCN requires a separate sequence generator than the other models because it needs an adjacency matrix to be generated. So the sequences generator is attatched with the GCN models.
