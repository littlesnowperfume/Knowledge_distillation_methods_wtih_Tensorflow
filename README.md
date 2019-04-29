# Knowledge Distillation Methods with Tensorflow
Knowledge distillation은 Teacher의 knowledge를 통해 student network를 개선하는 매우 효과적인 기법입니다.
최근까지 지속적으로 새로운 기법들이 제시되고 있지만 각 논문에서 선정하는 비교 기법과 네트워크 등이 전부 다릅니다.
또한 각 기법들이 각 저자에 의해 구현되었기 때문에 새로 knowledge distillation을 연구하려고 하면 각 기법들을 전부 찾아보거나 직접 구현해야하는 부담감이 있습니다.
이를 조금이나마 덜어드리고자, 다른 연구자들이 follow up할 수 있도록 제가 논문 제출을 위해 작성했던 코드를 군더더기를 최대한 제거하고 수정하기 쉽도록 만든 코드를 공개하고자 합니다.
지속적으로 새로운 기법들을 구현 및 추가할 계획이며, 모든 기법은 Tensorflow로 구현할 계획입니다.
아직 부족하지만 지속적으로 개선할 계획이며 언제든지 지적 및 조언 부탁드립니다.

(Sadly, my English skill is terribly low!! so please get patient to read my mess of words. :) )

Knowledge distillation is the method to enhance student network by teacher knowledge.
So annually knowledge distillation methods have been proposed but each paper's do experiments with different networks and compare with different methods.
And each method is implemented by each author, so if new researcher want to study about knowledge distillation, they have to find or implement all of methods. Surely it is very hard work.
To reduce this burden, I publish some code which are modified from my research codes for new researchers.
I'll update code and knowledge distillation algorithm, and all of things will be implemented by Tensorflow.
Now this repository is not so perfect but i will be improved, so please give some advise to be. (especially English.. :D)

# Implemented Knowledge Distillation Methods
구현된 기법들입니다. 각 분류법은 Seyed-Iman Mirzadeh et. al의 [TAKD](https://arxiv.org/abs/1902.03393)에서 영감을 얻어 만든 것입니다.
개인적으로 의미있는 분류라고 생각하여 작성하였습니다. 문제가 있다면 지적 부탁드립니다. :)

below methods are implemented and base on insight with [TAKD](https://arxiv.org/abs/1902.03393), I make each category. I think they are meaningful category, but if you think it has problem please notice for me :)

## Response-based Knowledge
- Soft-logit : [Geoffrey Hinton, et al. Distilling the knowledge in a neural network. arXiv:1503.02531, 2015.](https://arxiv.org/abs/1503.02531)

## Multi-connection Knowledge
- FitNet : [Adriana Romero, et al. Fitnets: Hints for thin deep nets. arXiv preprint arXiv:1412.6550, 2014.](https://arxiv.org/abs/1412.6550)
- Activation boundary (AB) : [Byeongho Heo, et. al. Knowledge transfer via distillation of activation boundaries formed by hidden neurons. AAAI2019](https://arxiv.org/abs/1811.03233)

## Shared-representation Knowledge
- Flow of Procedure (FSP) : [Junho Yim, et. al. A gift from knowledge distillation:
Fast optimization, network minimization and transfer learning. CVPR 2017.](http://openaccess.thecvf.com/content_cvpr_2017/html/Yim_A_Gift_From_CVPR_2017_paper.html)
- KD using Singular value decomposition(KD-SVD) : [Seung Hyun Lee, et. al. Self-supervised knowledge distillation using singular value decomposition. ECCV 2018](http://openaccess.thecvf.com/content_ECCV_2018/html/SEUNG_HYUN_LEE_Self-supervised_Knowledge_Distillation_ECCV_2018_paper.html)

# Expriment Results
직접 [ResNet](http://openaccess.thecvf.com/content_cvpr_2016/html/He_Deep_Residual_Learning_CVPR_2016_paper.html)을 통해 Teacher-Student networks를 구현 및 학습한 결과입니다.
이 실험 결과는 아직 발표되지 않은 제 연구 결과를 얻기 위한 구성으로 다른 기법들은 효과적으로 student network를 개선하지 못한 상황입니다.
이 결과는 충분한 hyper-parameter search를 거치지 않고 논문에 있는 것을 그대로 사용한 경우이며 만약 optimal hyper-parameter를 찾는 다면 이 결과는 달라질 수 있으니 참고로만 사용해주세요.

## Network architecture
Teacher는 ResNet-32, Student는 ResNet-8을 사용한 것으로 각 network는 tranining accuracy 기준으로 충분히 converged되었습니다.
모든 network를 학습하기 위한 hyper-parameter는 같으며 자세한 사항은 코드를 확인하시면 됩니다.

## Training/Validation plots
TBA

## Training/Validation plots
TBA


