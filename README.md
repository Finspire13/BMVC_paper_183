# BMVC_paper_183
Training &amp; inference code for BMVC2021 submission

## Enviroment
Pytorch == 1.1.0, torchvision == 0.3.0, python == 3.6 CUDA=10.1



## Reproduce our results
We provide the pretrained model that used to reproduce the results in our paper.
Download the dataset data.zip at https://mega.nz/#!O6wXlSTS!wcEoDT4Ctq5HRq_hV-aWeVF1_JB3cacQBQqOLjCIbc8  or https://zenodo.org/record/3625992#.Xiv9jGhKhPY . Unzip the data.zip file to the current folder, like xx.py, xx.py, data/.

Download the pre-trained models at https://disk.pku.edu.cn:443/link/3DBA0309F47A2A6C28543B25B3B8B2FF  Valid Until: 2023-04-03 23:59 to the current folder, like xx.py, xx.py, models/.

Run
```
python main.py --action=predict --dataset=50salads/gtea/breakfast --split=1/2/3/4/5
```
to get the predictions for each split. Then, run 
```
python eval.py  --dataset=50salads/gtea/breakfast
```
to get the evaluation results.


## Train the model 
Also, you can retrain the model by your self. Run
```
python main.py --action=train --dataset=50salads/gtea/breakfast --split=1/2/3/4/5
```

Note that the average results of each splits are reported in our paper. We recmmoand you to retrain the model for gtea or 50salads, because breakfast is too large and takes lots of time.
