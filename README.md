## InstructBLIP Finetune
This is the finetune of InstructBLIP [paper](http://arxiv.org/abs/2305.06500). 



### Install
```
git clone https://github.com/ZhanKunLiAuto/LAVIS-AD
cd LAVIS-AD
pip install -e .
```


### Prepare Vicuna Weights
InstructBLIP uses frozen 13B models. Please first follow the [instructions](https://github.com/lm-sys/FastChat) to prepare Vicuna v1.1 weights. 
Then modify the ```model.llm_model``` in the ```lavis/configs/models/blip2/blip2_instruct_vicuna13b_autonomous_driving.yaml``` to the folder that contains Vicuna weights.

### Train
```
python train.py --cfg-path lavis/configs/models/blip2/blip2_instruct_vicuna13b_autonomous_driving.yaml
```




### Demo
1. Modify the ```model.llm_model``` in the ```lavis/configs/models/blip2/blip2_instruct_vicuna13b.yaml``` to the folder that contains Vicuna weights.
2. Modify the ```model.pretrained``` in the ```lavis/configs/models/blip2/blip2_instruct_vicuna13b.yaml``` to the checkpoint.

3. Run Gradio Demo locally with ```python run_demo.py```
