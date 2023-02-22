### Best TTS based on BERT and VITS with some Natural Speech Features Of Microsoft

https://user-images.githubusercontent.com/16432329/220678182-4775dec8-9229-4578-870f-2eebc3a5d660.mp4


Based on BERT, NaturalSpeech, VITS

### Features
1, Hidden prosody embedding from BERT，get natural pauses in grammar

2, Infer loss from NaturalSpeech，get less sound error

3, Framework of VITS，get high audio quality

### Install

> pip install -r requirements.txt

> cd monotonic_align

> python setup.py build_ext --inplace

### Infer with Pretrained model

BaiduYun: https://pan.baidu.com/s/1Cj4MnwFyZ0XZmTR6EpygbQ?pwd=yn60

Google: https://drive.google.com/drive/folders/1sioiNpebOLyCmHURgOgJ7ppWI7b-7Rb5?usp=sharing

Or get from release page

put prosody_model.pt To ./bert/prosody_model.pt

put vits_bert_model.pth To ./vits_bert_model.pth

> python vits_infer.py

./vits_infer_out have the waves infered, listen !!!

### Train
download baker data: https://www.data-baker.com/data/index/TNtts/

change sample rate of waves, and put waves to ./data/waves

put 000001-010000.txt to ./data/000001-010000.txt

> python vits_prepare.py

> python train.py -c configs/bert_vits.json -m bert_vits

### Anther data Link
https://github.com/PlayVoice/HuaYan_TTS

### Video text
> 天空呈现的透心的蓝，像极了当年。总在这样的时候，透过窗棂，心，在天空里无尽的游弋！柔柔的，浓浓的，痴痴的风，牵引起心底灵动的思潮；情愫悠悠，思情绵绵，风里默坐，红尘中的浅醉，诗词中的优柔，任那自在飞花轻似梦的情怀，裁一束霓衣，织就清浅淡薄的安寂。
> 
> 风的影子翻阅过淡蓝色的信笺，柔和的文字浅浅地漫过我安静的眸，一如几朵悠闲的云儿，忽而氤氲成汽，忽而修饰成花，铅华洗尽后的透彻和靓丽，爽爽朗朗，轻轻盈盈
> 
> 时光仿佛有穿越到了从前，在你诗情画意的眼波中，在你舒适浪漫的暇思里，我如风中的思绪徜徉广阔天际，仿佛一片沾染了快乐的羽毛，在云环影绕颤动里浸润着风的呼吸，风的诗韵，那清新的耳语，那婉约的甜蜜，那恬淡的温馨，将一腔情澜染得愈发的缠绵。


