# Explainable Object Induced Action Decision For Autonomous Vehicle (CVPR 2020)

## BACKGROUND

---

* A paradigm for AV lies between **end-to-end approaches** and **pipelined approches**. 

    - **end-to-end approaches**: theoretically optimal, since all visual infos are used for decision-making. Need less data compared with pipelined method.
    
    - **pipelined approaches**: modularity, failure of a single module can compromise the the performance of the whole system. Have better interpretability, however modules may work themselves.

* Current datasets are too simple to determine the action vehicle should take.

## CONTRIBUTIONS

---

* A large dataset annotated for both driving commands and explanations.

* A new multi-task formulation of the action prediction problem that optimize for both the accuracy of action commands and explanations.

* A CNN architecture for the solution of this problem, combining reasoning about action-inducing object and global scene context.

* An experimental evaluation showing that the generation of explanations improves the decision making for action, and both benefit from a combination of object-centric and global scene reasoning.

## RELATED

---

* End-to-end learning for autonomous driving
    
    1. ALVINN system, first proposed, 1989: 
        > [29] Alvinn: An autonomous land vehicle in a neural network.

    2. end-to-end CNN to produce steering wheel commands:
        > [30] End to end learning for self-driving cars.

    3. take advantages of both context and object features:
        > [1] Interpretable learning for self-driving cars by visualizing causal attention.  
        >  
        > [2] End-to-end learning of driving models from large-scale video datasets. 
        >  
        > [3] Textual explanations for self-driving vehicles.  
        >  
        > [4] Monocular plan view networks for autonomous driving. (Train on simulator) 
        >  
        > [5] Deep object-centric policies for autonomous driving. (Train on simulator)  

* Global-local contextual representations  

    Contextual reasoning has a long history in computer vision:
    > [31] Searching for objects driven by context.
    >  
    > [32] Contextual action recognition with r* cnn.
    > 
    > [33] Deep object-centric representations for generalizable robot learning.
    >
    > [34] A unified multi-scale deep convolutional neural network for fast object detection.
    >
    > [35] Zoom-net: Mining deep feature interactions for visual relationship recognition.
    > 
    > [36] Graph r-cnn for scene graph generation.
    >
    > [37] Videos as space-time region graphs.

    1. e.g. multi-scale pooling improves Faster-RCNN and Zoom-net:
        > [34] A unified multi-scale deep convolutional neural network for fast object detection.
        >  
        > [35] Zoom-net: Mining deep feature interactions for visual relationship recognition.
    
    However contextual learning has received limited attention in AV:

    1. proposed a selector but neglect the global feature:
        > [5] Deep object-centric policies for autonomous driving.

    2. Consider whole scene feature but ignore object:
        > [1] Interpretable learning for self-driving cars by visualizing causal attention.
        > 
        > [3] extual explanations for self-driving vehicles.

* Attention mechanisms

    Widely used in neural network:
    > [39] Show, attend and tell: Neural image caption generation with visual attention.
    > 
    > [40] Residual attention network for image classification.

    Attention map to visualize inner working of networks:
    > [24] Deep inside convolutional networks: Visualising image classification models and saliency maps.
    > 
    > [25] Visualizing and understanding convolutional networks.
    >
    > [26] Decoupled deep neural network for semi-supervised semantic segmentation.
    > 
    > [27] Grad-cam: Visual explanations from deep networks via gradient-based localization.
    >
    > [28] Multimodal explanations: Justifying decisions and pointing to the evidence.

    In AV:

    1. develope a richer notion of attention on pixels:
        > [41] Visualbackprop: visualizing cnns for autonomous driving.

    2. using eye tracking systems to get interest regions:
        > [18] Predicting driver attention in critical situations.
        > 
        > [19] Predicting the driver’s focus of attention: the dr(eye)ve project.

* Explanations

    Textual explanation for insight on network understanding of images or scene:
    > [42] Deep Learning.

    1. e.g. generate text to explain either attention maps or network predictions:
        > [16] Context-aware captions from context-agnostic supervision.
        > 
        > [17] Grounding visual explanations.
        > 
        > [39] Show, attend and tell: Neural image caption generation with visual attention.

* Datasets

    - KITTI  
    Object BBox, semantic segementation labels, depth, 3D point clouds
    
    - BDD100K  
    100K videos annotated with image level labels, object BBox, drivale areas, lane markings, full-frame instance segmentation

    - Apolloscape  
    140K images, RGB videos and corresponding dense 3D point clouds with focus on 3D labeling and semantic segmentation.

    - nuScenes  
    1000 scenes with sensor information produced by camera, LiDAR, and radar.

## DETAILS

---

## EXPERIMENTS

---

## RESOURCE

---

* [Paper](https://openaccess.thecvf.com/content_CVPR_2020/papers/Xu_Explainable_Object-Induced_Action_Decision_for_Autonomous_Vehicles_CVPR_2020_paper.pdf)
