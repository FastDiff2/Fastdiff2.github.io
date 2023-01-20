

{:.no_toc}
* toc
{:toc}
## Abstract

  Generative adversarial networks and denoising probabilistic models have recently achieved impressive performances in image and audio synthesis. After revisiting their success in conditional speech synthesis, we find that 1) GANs sacrifice sample diversity for quality and speed, 2) diffusion models exhibit outperformed sample quality and diversity while requiring a large number of iterative refinements. Achieving high-quality and diverse speech synthesis at a low computational cost has become an open problem for all neural synthesizers. In this work, we propose to converge advantages from GANs and diffusion models by incorporating both classes, introducing dual-empowered modeling perspectives: 1) DiffGAN-Wave, a diffusion model whose denoising process is parametrized by conditional GANs, and the non-Gaussian denoising distribution makes it much more stable to implement the reverse process with large steps sizes; and 2) GANDiff-Wave, a generative adversarial network whose forward process is constructed by multiple denoising diffusion iterations, which exhibits better sample diversity than traditional GANs. Experimental results show that both variants enjoy an efficient 4-step sampling process and demonstrate superior sample quality and diversity. Audio samples are available at https://RevisitSpeech.github.io
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
			<th style="text-align: center">DiffGAN-Wave</th>
            <th style="text-align: center">GANDiff-Wave</th>
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
			<th style="text-align: center">DiffGAN-Wave</th>
            <th style="text-align: center">GANDiff-Wave</th>
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
			<th style="text-align: center">DiffGAN-Wave</th>
            <th style="text-align: center">GANDiff-Wave</th>
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
			<th style="text-align: center">DiffGAN-Wave</th>
            <th style="text-align: center">GANDiff-Wave</th>
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
			<th style="text-align: center">DiffGAN-Wave</th>
            <th style="text-align: center">GANDiff-Wave</th>
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



## Ablation Study

<ruby>Text: in being comparatively modern.</ruby>
<table>
	<thead>
		<tr>
			<th style="text-align: center">DiffGAN-Wave</th>
            <th style="text-align: center">w/o Diffusion Reparameterization</th>
            <th style="text-align: center">w/o Reconstruction Objective</th>
            <th style="text-align: center">GANDiff-Wave</th>
            <th style="text-align: center">w/o Reconstruction Objective</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Ablation/diffgan/001.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Ablation/diffgan_w_o_DR/001.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Ablation/diffgan_w_o_RB/001.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Ablation/gandiff/001.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Ablation/gandiff_w_o_DR/001.wav" type="audio/wav"></audio></td>
		</tr>
	</tbody>
</table>

<ruby>Text: it is of the first importance that the letter used should be fine in form.</ruby>
<table>
	<thead>
		<tr>
			<th style="text-align: center">DiffGAN-Wave</th>
            <th style="text-align: center">w/o Diffusion Reparameterization</th>
            <th style="text-align: center">w/o Reconstruction Objective</th>
            <th style="text-align: center">GANDiff-Wave</th>
            <th style="text-align: center">w/o Reconstruction Objective</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Ablation/diffgan/002.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Ablation/diffgan_w_o_DR/002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Ablation/diffgan_w_o_RB/002.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Ablation/gandiff/002.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Ablation/gandiff_w_o_DR/002.wav" type="audio/wav"></audio></td>
		</tr>
	</tbody>
</table>

<ruby>Text: the middle ages brought calligraphy to perfection , and it was natural therefore.</ruby>
<table>
	<thead>
		<tr>
			<th style="text-align: center">DiffGAN-Wave</th>
            <th style="text-align: center">w/o Diffusion Reparameterization</th>
            <th style="text-align: center">w/o Reconstruction Objective</th>
            <th style="text-align: center">GANDiff-Wave</th>
            <th style="text-align: center">w/o Reconstruction Objective</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Ablation/diffgan/003.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Ablation/diffgan_w_o_DR/003.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Ablation/diffgan_w_o_RB/003.wav" type="audio/wav"></audio></td>
			<td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Ablation/gandiff/003.wav" type="audio/wav"></audio></td>
            <td style="text-align: center"><audio controls style="width: 150px;"><source src="wavs/Ablation/gandiff_w_o_DR/003.wav" type="audio/wav"></audio></td>
		</tr>
	</tbody>
</table>
