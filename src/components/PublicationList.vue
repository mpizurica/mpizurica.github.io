<template>
    <button class="mb-5 link tooltip"> [Google Scholar]<span class="tooltiptext">coming soon!</span></button>
    <div class="flex flex-col space-y-5"> 
        <div class="grid grid-cols-5">
            <div class=" md:col-span-1 col-span-5 text-lg">
                <p class="list-info w-full"> Preprint </p>
            </div>
            <div class="md:col-span-4 col-span-5 text-lg">
                <p>WSI based prediction of <span class='italic'>TP53</span> mutations identifies aggressive disease phenotype in prostate cancer 
                    <button class="link tooltip">[pdf]<span class="tooltiptext">coming soon!</span></button>
                    <button class="link"><a href="https://github.com/mpizurica/WSI_mut">[code]</a></button>
                </p>
                <p class="pt-1 text-sm"> <span class="underline">Marija Pizurica</span>, Maarten Larmuseau, Kim Van der Eecken, Francisco Carrillo-Perez,
                     Louise de Schaetzen van Brienen, Nicolaas Lumen, Jo Van Dorpe, Piet Ost, Sofie Verbeke, Olivier Gevaert<sup>*</sup> 
                     and Kathleen Marchal<sup>*</sup></p>

                <button class="pt-1 text-sm" v-on:click="expanded = !expanded">{{expanded? '&#x21E1; hide' : '&#x21E2; show'}} abstract</button> 

                <div v-show="expanded" class="pt-1 text-sm abstract">
                    <p>
                        In prostate cancer, there is an urgent need for objective prognostic biomarkers that identify 
                        a tumor's metastatic potential at an early stage. While recent analyses indicated TP53 mutations 
                        as candidate biomarker, molecular profiling in a clinical setting is complicated by 
                        the heterogeneity of prostate tumors. Deep learning models that can predict the presence 
                        of TP53 mutations from Whole Slide Images (WSIs) offer the potential to solve the heterogeneity 
                        issue encountered during marker profiling.  Although  previous studies show how these models 
                        achieve reasonable performance at patient level, it has not yet been validated whether they 
                        can also correctly indicate the region with the highest load of the predicted mutation within 
                        a heterogenous solid tumor. In addition, no in-depth assessment has been performed to explain 
                        the possible origin of the FP or FN predictions of these models, while such interpretations 
                        are imperative for their implementation in practice.</p>
                        
                        <p>
                        Here we developed TiDo, a deep learning model that achieves state-of-the-art performance 
                        in predicting TP53 mutations from WSIs of primary prostate tumors. On an independent
                        multi-focal cohort, we could not only show successful generalization of the model, but 
                        also indicate within a tumor the regions with the highest prevalence of TP53 mutations. 
                        In addition, in-depth molecular analysis of the predictions shows that, by training on 
                        the label TP53 mutation, our model captures a molecular phenotype that is representative for 
                        aggressive disease triggered by, but not restricted to TP53 mutations. This indicates that 
                        features derived from WSIs cannot only facilitate molecular profiling of TP53 mutations by 
                        indicating the regions on The WSI with the highest mutational TP53 load, but have the 
                        potential to become the next-generation, in-silico biomarkers for prostate cancer prognosis</p>
                </div>
                
                <div class="h-55 mt-2">
                    <img class="h-full w-full shadow-md object-cover rounded-xl" src="../assets/WSI_mut.jpg" alt="">
                </div>
            </div>
        </div>
        <div class="grid grid-cols-5">
            <div class=" md:col-span-1 col-span-5 text-lg">
                <p class="list-info w-full">BIOCOMP `22</p>
            </div>
            <div class="md:col-span-4 col-span-5 text-lg">
                <p>Self-supervised multimodal pre-training for lung adenocarcinoma overall survival prediction 
                    <button class="link tooltip">[pdf]<span class="tooltiptext">coming soon!</span></button>
                    <button class="link"><a href="https://github.com/pacocp/SSL-Survival"> [code] </a></button>
                </p>
                <p class="pt-1 text-sm">Francisco Carrillo-Perez<sup>*</sup>, <span class="underline">Marija Pizurica</span><sup>*</sup>, Ignacio Rojas, Kathleen Marchal, 
                                        Luis Javier Herrera and Olivier Gevaert
                </p>

                <button class="pt-1 text-sm" v-on:click="expanded_ssl = !expanded_ssl">{{expanded_ssl? '&#x21E1; hide' : '&#x21E2; show'}} abstract</button> 
                <div v-show="expanded_ssl" class="pt-1 text-sm abstract">
                    <p>
                        The collection of multiple modalities of cancer data has increased over the years, allowing research in complex problems such as cancer prognosis. However, given the high-dimensionality of biological data, efficiently training machine learning models when scarce samples are available is still challenging. In this work we propose a novel multimodal self-supervised learning framework based on neural networks for survival analysis and we evaluate it in a few-shot learning setting for lung adenocarcinoma prognosis. We show that the multimodal self-supervised pre-training is more effective than regular pre-training or training from scratch for two modalities (RNA-Seq and Whole Slide Imaging) when few samples are available. With the multimodal self-supervised learning framework, the relation between the modalities is learned in a pretext task and the leveraged information is successfully used for the relevant downstream task for both modalities, showing the potential of the proposed methodology.</p>
                </div>

                <div class="h-55 mt-2">
                    <img class="h-full w-full shadow-md object-cover rounded-xl" src="../assets/SSL_im.jpg" alt="">
                </div>
            </div>
        </div>
        <div class="grid grid-cols-5">
            <div class=" md:col-span-1 col-span-5 text-lg">
                <p class="list-info w-full">Preprint</p>
            </div>
            <div class="md:col-span-4 col-span-5 text-lg">
                <p>Synthetic whole-slide image tile generation with gene expression profiles infused deep generative models
                    <button class="link tooltip">[pdf]<span class="tooltiptext">coming soon!</span></button>
                    <button class="link"><a href="https://github.com/gevaertlab/RNA-GAN"> [code] </a></button>
                </p>
                <p class="pt-1 text-sm">Francisco Carrillo-Perez, <span class="underline">Marija Pizurica</span>, Michael G.
                                        Ozawa, Hannes Vogel, Robert B. West, Christina S.
                                        Kong, Jeanne Shen and Olivier Gevaert
                </p>

                <button class="pt-1 text-sm" v-on:click="expanded_rna_gan = !expanded_rna_gan">{{expanded_ssl? '&#x21E1; hide' : '&#x21E2; show'}} abstract</button> 
                <div v-show="expanded_rna_gan" class="pt-1 text-sm abstract">
                    <p>The acquisition of multi-modal biological data such as RNA sequencing and whole 
                            slide imaging (WSI) for the same sample has increased
                            in recent years, enabling studying human biology from multiple angles.
                            However, despite these emerging multi-modal efforts, for the majority
                            of studies only one modality is typically available due to financial or
                            logistical constraints. Given these difficulties, multi-modal data imputation 
                            and multi-modal synthetic data are appealing as a solution for the
                            multi-modal data scarcity problem. Currently, most studies focus on generating 
                            a single modality (e.g. WSI), without leveraging the information
                            provided by additional data modalities (e.g. gene expression profiles). In
                            this work, we propose an approach to generate WSI tiles by using deep
                            generative models infused with matched gene expression profiles. First,
                            we train a variational autoencoder (VAE) that learns a latent representation of 
                            multi-tissue gene expression profiles, and we show that this
                            model is able to generate realistic synthetic gene expression. Then, we
                            use this representation to infuse generative adversarial networks (GAN),
                            generating lung and brain cortex tissue tiles with a new model that we
                            call RNA-GAN. Tiles generated by RNA-GAN were preferred by expert pathologists 
                            in comparison to tiles generated using traditional GANs
                            and RNA-GAN needs fewer training epochs to generate high-quality
                            tiles. In addition, RNA-GAN was able to generalize to gene expression profiles 
                            outside of the training set, showing imputation capabilities.
                            A web-based quiz is available for users to play a game distinguishing
                            real and synthetic tiles: https://rna-gan.stanford.edu/ and the code for
                            RNA-GAN is available here: https://github.com/gevaertlab/RNA-GAN.
                </p>
                </div>

                <div class="h-55 mt-2">
                    <img class="h-full w-full shadow-md object-cover rounded-xl" src="../assets/SSL_im.jpg" alt="">
                </div>
            </div>
        </div>
        <div class="grid grid-cols-5">
            <div class=" md:col-span-1 col-span-5 text-lg">
                <p class="list-info w-full">Preprint</p>
            </div>
            <div class="md:col-span-4 col-span-5 text-lg">
                <p>RNA-to-image pan-cancer synthesis using cascaded diffusion models
                    <button class="link tooltip">[pdf]<span class="tooltiptext">coming soon!</span></button>
                    <button class="link tooltip">[code]<span class="tooltiptext">coming soon!</span></button>
                </p>
                <p class="pt-1 text-sm">Francisco Carrillo-Perez, <span class="underline">Marija Pizurica</span>, Yuanning Zheng and Olivier Gevaert
                </p>

                <button class="pt-1 text-sm" v-on:click="expanded_diff = !expanded_diff">{{expanded_ssl? '&#x21E1; hide' : '&#x21E2; show'}} abstract</button> 
                <div v-show="expanded_diff" class="pt-1 text-sm abstract">
                    <p>[coming soon]</p>
                </div>

                <div class="h-55 mt-2">
                    <img class="h-full w-full shadow-md object-cover rounded-xl" src="../assets/SSL_im.jpg" alt="">
                </div>
            </div>
        </div>
        <div class="grid grid-cols-5">
            <div class=" md:col-span-1 col-span-5 text-lg">
                <p class="list-info w-full">AT4SSL `21</p>
            </div>
            <div class="md:col-span-4 col-span-5 text-lg">
                <p>Frozen Pretrained Transformers for Neural Sign Language Translation 
                    <button class="link"><a href="https://aclanthology.org/2021.mtsummit-at4ssl.10.pdf"> [pdf] </a></button>
                    <button class="link"><a href="https://github.com/m-decoster/fpt4slt"> [code] </a></button>
                </p>
                <p class="pt-1 text-sm">Mathieu De Coster, Karel D'Oosterlinck, <span class="underline">Marija Pizurica</span>, Paloma Rabaey, Severine
                    Verlinden, Mieke Van Herreweghe, Joni Dambre</p>

                <button class="pt-1 text-sm" v-on:click="expanded_fpt = !expanded_fpt">{{expanded_fpt? '&#x21E1; hide' : '&#x21E2; show'}} abstract</button> 
                <div v-show="expanded_fpt" class="pt-1 text-sm abstract">
                    <p>
                        One of the major challenges in sign language translation from a sign language to a spoken language is the lack of parallel corpora. Recent works have achieved promising results on the RWTH-PHOENIX-Weather 2014T dataset, which consists of over eight thousand parallel sentences between German sign language and German. However, from the perspective of neural machine translation, this is still a tiny dataset. To improve the performance of models trained on small datasets, transfer learning can be used. While this has been previously applied in sign language translation for feature extraction, to the best of our knowledge, pretrained language models have not yet been investigated. We use pretrained BERT-base and mBART-50 models to initialize our sign language video to spoken language text translation model. To mitigate overfitting, we apply the frozen pretrained transformer technique: we freeze the majority of parameters during training. Using a pretrained BERT model, we outperform a baseline trained from scratch by 1 to 2 BLEU-4. Our results show that pretrained language models can be used to improve sign language translation performance and that the self-attention patterns in BERT transfer in zero-shot to the encoder and decoder of sign language translation models.</p>
                </div>
            </div>
        </div>
        
    </div>
</template>

<script>
    export default {
        data() {
            return {
                expanded: false,
                expanded_ssl: false,
                expanded_fpt: false,
                expanded_rna_gan: false,
                expanded_diff: false

            }
        }
}</script>

<style scoped>
.abstract{
    text-align: justify;
}    

/* Tooltip container */
.tooltip {
  position: relative;
  display: inline-block;
  border-bottom: 0px dotted black; /* If you want dots under the hoverable text */
}

/* Tooltip text */
.tooltip .tooltiptext {
  visibility: hidden;
  width: 120px;
  background-color: rgba(187, 187, 187);
  color: #fff;
  text-align: center;
  padding: 5px 0;
  border-radius: 6px;
 
  /* Position the tooltip text - see examples below! */
  position: absolute;
  z-index: 1;

  width: 120px;
  bottom: 100%;
  left: 50%;
  margin-left: -60px; /* Use half of the width (120/2 = 60), to center the tooltip */
}

.tooltip .tooltiptext::after {
  content: "";
  position: absolute;
  top: 100%;
  left: 50%;
  margin-left: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: rgb(187, 187, 187) transparent transparent transparent;
}

/* Show the tooltip text when you mouse over the tooltip container */
.tooltip:hover .tooltiptext {
  visibility: visible;
}

</style>