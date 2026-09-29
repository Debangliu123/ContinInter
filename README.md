<div align="center">

# CONTININTER

### State-Space and Attention-Aware Audio-Visual Continuous Interaction Modeling for Efficient Speech Separation

**Debang Liu<sup>†</sup>, Tianqi Zhang, Chen Yi, and Ying Wei**

School of Communications and Information Engineering  
Chongqing University of Posts and Telecommunications, Chongqing, China

</div>

---

## Our Method

We propose **ContinInter**, an efficient audio-visual speech separation framework designed to continuously exploit complementary audio and visual information across different resolutions, network layers, and modalities.

ContinInter contains two core components: the **Interactive State-Aware Model (ISAM)** and **Multi-Scale Attentive State-Space Sequence Modeling (MASS)**. ISAM embeds cross-attention into convolutional state-space modeling to enable continuous cross-modal interaction, whereas MASS combines temporal-channel enhancement, DWT-SSM, and self-attention to jointly capture local structures, long-range dependencies, and global context.

Experimental results on GRID-Mix, LRS2-Mix, and LRS3-Mix demonstrate that ContinInter achieves near-best separation performance at its level of computational efficiency while maintaining a favorable balance among model size, computational cost, and training cost.

---

## Network Architecture

### Main Framework

ContinInter adopts a multi-scale encoder-decoder architecture for time-domain audio-visual speech separation. The encoded audio and visual features are first processed by separate MASS branches to strengthen their modality-specific contextual representations.

ISAM then performs continuous audio-visual interaction across different resolutions and network layers. After cross-modal fusion, an audio-visual MASS branch further models the fused sequence for mask estimation and waveform reconstruction.

<!--
Upload the overall architecture figure to:

picture/ContinInter_framework.png

Then replace the text below with:

<p align="center">
  <img src="picture/ContinInter_framework.png" width="95%">
</p>
-->

<p align="center">
  <b>The overall ContinInter architecture will be added here.</b>
</p>

---

### Interactive State-Aware Model

The **Interactive State-Aware Model (ISAM)** consists of stacked Cross-Modal Dynamic State Blocks and an Adaptive Gated Fusion module.

Each dynamic state block embeds cross-attention into convolutional state-space modeling. Cross-attention establishes associations between heterogeneous audio and visual features, while DWT-SSM captures temporal dependencies within the interacted representations. Through block stacking, ISAM continuously refines cross-modal relationships across multiple resolutions and network layers.

Adaptive gated fusion subsequently selects and combines complementary information from the audio and visual representations.

<!--
Upload the ISAM figure to:

picture/ISAM.png

Then replace the text below with:

<p align="center">
  <img src="picture/ISAM.png" width="80%">
</p>
-->

<p align="center">
  <b>The ISAM architecture will be added here.</b>
</p>

---

### Multi-Scale Attentive State-Space Sequence Modeling

The **Multi-Scale Attentive State-Space Sequence Modeling (MASS)** network integrates a Temporal-Channel Enhancement Block, DWT-SSM, self-attention, and residual connections.

The Temporal-Channel Enhancement Block strengthens target-related temporal-channel features. DWT-SSM combines dilated depthwise temporal convolution with selective state-space modeling to efficiently capture local structures and long-range dependencies. Self-attention further models global relationships among sequence features.

Through multi-layer stacking, MASS progressively integrates local structures, temporal-channel responses, long-range state dependencies, and global contextual information.

<!--
Upload the MASS figure to:

picture/MASS.png

Then replace the text below with:

<p align="center">
  <img src="picture/MASS.png" width="80%">
</p>
-->

<p align="center">
  <b>The MASS architecture will be added here.</b>
</p>

---

## Results

ContinInter is evaluated on three audio-visual speech separation benchmarks:

- **GRID-Mix**
- **LRS2-Mix**
- **LRS3-Mix**

The experimental results demonstrate that ContinInter:

- effectively exploits complementary audio-visual information;
- achieves near-best separation performance at its level of computational efficiency;
- maintains a compact model size and low computational cost;
- reduces training memory consumption;
- achieves a favorable balance between separation performance and efficiency.

<!--
Upload the experimental comparison figure to:

picture/performance_comparison.png

Then add:

<p align="center">
  <img src="picture/performance_comparison.png" width="90%">
</p>
-->

---

## Demo
This video is used to demonstrate the effectiveness of our model for speech separation on selected real-world recordings:

https://github.com/user-attachments/assets/bf8b7764-7fbd-4866-8d99-ea22ac9cfd66


<!--
After uploading a demonstration video to GitHub, paste the generated
GitHub attachment URL directly below the corresponding title.

### Example 1

**Input mixture**

https://github.com/user-attachments/assets/your-mixture-video-id

**Separated speaker 1**

https://github.com/user-attachments/assets/your-speaker1-video-id

**Separated speaker 2**

https://github.com/user-attachments/assets/your-speaker2-video-id
-->

<p align="center">
  <b>Audio-visual separation demonstrations are coming soon.</b>
</p>

---

## Citation

If ContinInter is useful for your research, please cite our work:

```bibtex
@misc{liu2026contininter,
  title  = {ContinInter: State-Space and Attention-Aware Audio-Visual
            Continuous Interaction Modeling for Efficient Speech Separation},
  author = {Liu, Debang and Zhang, Tianqi and Yi, Chen and Wei, Ying},
  year   = {2026},
  note   = {Manuscript}
}
```

The citation information will be updated after publication.

---




<div align="center">

If you find this project useful, please consider giving it a ⭐.

</div>
