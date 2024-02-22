Requirements
Python 3.6+
Pytorch>=1.6
torchvision>=0.7.0
einops
matplotlib
cv2
scipy
tqdm
scikit

Training Commands
The train/val data pathes are set in data/init.py
# x4
python demo_train.py --model=CSARST --dataset=UCMerced --scale=4 --patch_size=192 --ext=img
# x3
python demo_train.py --model=CSARST --dataset=UCMerced --scale=3 --patch_size=144 --ext=img
# x2
python3 demo_train.py --model=CSARST --dataset=UCMerced --scale=2 --patch_size=96 --ext=img 

Testing Commands
The test data path and the save path can be edited in demo_deploy.py
# x4
python demo_deploy.py --model=CSARST --scale=4
# x3
python demo_deploy.py --model=CSARST --scale=3
# x2
python3 demo_deploy.py --model=CSARST --scale=2

Compute the evaluated results in term of PSNR and SSIM, where the SR/HR paths can be edited in calculate_PSNR_SSIM.py

cd metric_scripts 
python3 calculate_PSNR_SSIM.py
