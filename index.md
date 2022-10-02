

{:.no_toc}
* toc
{:toc}
## Abstract

FastDiff, as a class of denoising probabilistic models, has recently achieved impressive performances in speech synthesis. It utilizes a noise predictor to learn a tight inference schedule for skipping denoising steps. Despite the successful speedup of FastDiff, there is still room for improvements, e.g., further optimizing the speed-quality trade-off and accelerating DDPMs training procedures. After analyzing GANs and diffusion models in conditional speech synthesis, we find that: GANs produce samples but do not cover the whole distribution, and the coverage degree does not distinctly impact audio quality. Inspired by these observations, we propose to trade off diversity for quality and speed by incorporating GANs into diffusion models, introducing two GAN-empowered modeling perspectives: (1) FastDiff 2 (Diff-GAN), whose denoising distribution is parametrized by conditional GANs; and (2) FastDiff 2 (GAN-Diff), in which the denoising model is treated as a generator in GAN for adversarial training. Unlike the acceleration methods based on skipping the denoising steps, FastDiff 2 provides a principled way to speed up both the training and inference processes. Experimental results demonstrate that both variants of FastDiff 2 enjoy an efficient 4-step sampling process as in FastDiff yet demonstrate a superior sample quality.

## Comparison with other models

<ruby>Text: in being comparatively modern.</ruby>
<table>
	<thead>
		<tr>
			<th style="text-align: center">GT</th>
            <th style="text-align: center">WaveNet</th>
			<th style="text-align: center">WaveGlow</th>
			<th style="text-align: center">HIFI-GAN</th>
            <th style="text-align: center">UnivNet</th>
			<th style="text-align: center">Diffwave</th>
			<th style="text-align: center">WaveGrad</th>
            <th style="text-align: center">FastDiff</th>
			<th style="text-align: center">FastDiff 2 (Diff-GAN)</th>
            <th style="text-align: center">FastDiff 2 (GAN-Diff)</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/GT/001.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/WaveNet/001.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/WaveGlow/001.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/HIFIGAN/001.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/UnivNet/001.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/Diffwave/001.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/WaveGrad/001.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/FastDiff/001.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/diffusion_leverage_GAN/001.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/GAN_leverage_diffusion/001.wav" type="audio/wav"></audio></td>
		</tr>
	</tbody>
</table>

<ruby>Text: it is of the first importance that the letter used should be fine in form.</ruby>
<table>
	<thead>
		<tr>
			<th style="text-align: center">GT</th>
            <th style="text-align: center">WaveNet</th>
			<th style="text-align: center">WaveGlow</th>
			<th style="text-align: center">HIFI-GAN</th>
            <th style="text-align: center">UnivNet</th>
			<th style="text-align: center">Diffwave</th>
			<th style="text-align: center">WaveGrad</th>
            <th style="text-align: center">FastDiff</th>
			<th style="text-align: center">FastDiff 2 (Diff-GAN)</th>
            <th style="text-align: center">FastDiff 2 (GAN-Diff)</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/GT/002.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/WaveNet/002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/WaveGlow/002.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/HIFIGAN/002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/UnivNet/002.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/Diffwave/002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/WaveGrad/002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/FastDiff/002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/diffusion_leverage_GAN/002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/GAN_leverage_diffusion/002.wav" type="audio/wav"></audio></td>
		</tr>
	</tbody>
</table>

<ruby>Text: the middle ages brought calligraphy to perfection , and it was natural therefore.</ruby>
<table>
	<thead>
		<tr>
			<th style="text-align: center">GT</th>
            <th style="text-align: center">WaveNet</th>
			<th style="text-align: center">WaveGlow</th>
			<th style="text-align: center">HIFI-GAN</th>
            <th style="text-align: center">UnivNet</th>
			<th style="text-align: center">Diffwave</th>
			<th style="text-align: center">WaveGrad</th>
            <th style="text-align: center">FastDiff</th>
			<th style="text-align: center">FastDiff 2 (Diff-GAN)</th>
            <th style="text-align: center">FastDiff 2 (GAN-Diff)</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/GT/003.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/WaveNet/003.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/WaveGlow/003.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/HIFIGAN/003.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/UnivNet/003.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/Diffwave/003.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/WaveGrad/003.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/FastDiff/003.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/diffusion_leverage_GAN/003.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Comparision/GAN_leverage_diffusion/003.wav" type="audio/wav"></audio></td>
		</tr>
	</tbody>
</table>

## Model Generalization

<ruby>Text: Ask her to bring these things with her from the store.</ruby>
<table>
	<thead>
		<tr>
			<th style="text-align: center">GT</th>
            <th style="text-align: center">WaveNet</th>
			<th style="text-align: center">WaveGlow</th>
			<th style="text-align: center">HIFI-GAN</th>
            <th style="text-align: center">UnivNet</th>
			<th style="text-align: center">Diffwave</th>
			<th style="text-align: center">WaveGrad</th>
            <th style="text-align: center">FastDiff</th>
			<th style="text-align: center">FastDiff 2 (Diff-GAN)</th>
            <th style="text-align: center">FastDiff 2 (GAN-Diff)</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/GT/001.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/WaveNet/001.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/WaveGlow/001.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/HIFIGAN/001.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/UnivNet/001.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/Diffwave/001.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/WaveGrad/001.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/FastDiff/001.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/Diffusion_leverage_GAN/001.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/GAN_leverage_diffusion/001.wav" type="audio/wav"></audio></td>
		</tr>
	</tbody>
</table>



<ruby>Text: Please call Stella.</ruby>
<table>
	<thead>
		<tr>
			<th style="text-align: center">GT</th>
            <th style="text-align: center">WaveNet</th>
			<th style="text-align: center">WaveGlow</th>
			<th style="text-align: center">HIFI-GAN</th>
            <th style="text-align: center">UnivNet</th>
			<th style="text-align: center">Diffwave</th>
			<th style="text-align: center">WaveGrad</th>
            <th style="text-align: center">FastDiff</th>
			<th style="text-align: center">FastDiff 2 (Diff-GAN)</th>
            <th style="text-align: center">FastDiff 2 (GAN-Diff)</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/GT/002.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/WaveNet/002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/WaveGlow/002.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/HIFIGAN/002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/UnivNet/002.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/Diffwave/002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/WaveGrad/002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/FastDiff/002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/Diffusion_leverage_GAN/002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Generalization/GAN_leverage_diffusion/002.wav" type="audio/wav"></audio></td>
		</tr>
	</tbody>
</table>
