# ece1512_mamba
Unsuccessful attempt to use Mamba for sea clutter prediction.

Installation in a Jupyter environment as follows:
```
!pip install torch==2.4.0 torchvision==0.19.0 torchaudio==2.4.0 --index-url https://download.pytorch.org/whl/cu121
!pip install causal-conv1d==1.4.0
!pip install mamba-ssm==2.2.2
!pip install netCDF4
```
Code will run on Google Colab. Note that GPU must be used for Mamba to run.

Relevant sources:
- Sea Clutter Dataset File 20210106155330\01\staring was obtained from the SDRSDP dataset as cited below. Note that a WeChat account is required to download the dataset.


```bibtex
@misc{sdrdsp, title={雷达对海探测数据 2020年第1期 [Radar Maritime Detection Data, Issue 1, 2020]}, url={https://radars.ac.cn/web/data/getData?newsColumnId=09f293d5-a918-45a5-bf78-2bf74c582ea7}, journal={雷达学报 [Journal of Radar]}, publisher={雷达学报 [Journal of Radar]}, author={Liu, Ningbo and Ding, Hao and Huang, Yong and Dong, Yunlong and Wang, Guoqing and Dong, Kai}} 

```

We attempted to use S-Mamba, which is available as follows:
```bibtex
@article{wang2025_s_mamba,
  title={Is mamba effective for time series forecasting?},
  author={Wang, Zihan and Kong, Fanheng and Feng, Shi and Wang, Ming and Yang, Xiaocui and Zhao, Han and Wang, Daling and Zhang, Yifei},
  journal={Neurocomputing},
  volume={619},
  pages={129178},
  year={2025},
  publisher={Elsevier}
}

@misc{
s_mamba_code, 
url={https://github.com/wzhwzhwzh0921/S-D-Mamba}, 
 title={Is Mamba Effective for Time Series Forecasting? [GitHub Repository]},
  author={Wang, Zihan and Kong, Fanheng and Feng, Shi and Wang, Ming and Yang, Xiaocui and Zhao, Han and Wang, Daling and Zhang, Yifei},
} 
```

Unfortunately, the results displayed likely suffer from cross-contaimination between train/test samples, and the model performs poorly when translated to unseen rangebins. Further investigation will be required to evaluate whether Mamba is a suitable model for sea clutter prediction.
