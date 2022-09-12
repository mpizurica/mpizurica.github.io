<template>
    <button class="mb-5 link"> [Google Scholar]</button>
    <div class="flex flex-col space-y-5">
        <div class="grid grid-cols-5">
            <div class=" md:col-span-1 col-span-5">
                <p class="list-info w-full"> Preprint </p>
            </div>
            <div class="md:col-span-4 col-span-5">
                <p>WSI based prediction of <span class='italic'>TP53</span> mutations identifies aggressive disease phenotype in prostate cancer 
                    <button class="link">[pdf]</button>
                    <button class="link"><a href="https://github.com/mpizurica/WSI_mut">[code]</a></button>
                </p>
                <p class="pt-1 text-xs">Marija Pizurica, Maarten Larmuseau, Kim Van der Eecken, Francisco Carrillo-Perez,
                     Louise de Schaetzen van Brienen, Nicolaas Lumen, Jo Van Dorpe, Piet Ost, Sofie Verbeke, Olivier Gevaert<sup>*</sup> 
                     and Kathleen Marchal<sup>*</sup></p>

                <button class="pt-1 text-xs" v-on:click="expanded = !expanded">{{expanded? '&#x21E1; hide' : '&#x21E2; show'}} abstract</button> 

                <div v-show="expanded" class="pt-1 text-xs abstract">
                    <p>
                    Recent studies have shown the potential of deep learning models to predict the presence of certain oncogenic 
                    mutations from histopathological slides. However, thorough interpretations of the reasoning behind predictions 
                    and decisions made by these models is still lacking in current research, while such interpretations are imperative 
                    for their implementation in practice.</p>
                    
                    <p>
                    This work is the first to provide an in-depth molecular analysis of the prediction results of TiDo, 
                    a state-of-the-art model we developed for TP53 mutation prediction from histopathology slides of prostate cancer. 
                    The model successfully generalizes to our in-house, multi-focal cohort of advanced prostate cancer and even the 
                    associated metastatic lymph nodes. Our molecular analysis identified several important biological pathways 
                    affecting stromal composition that are related to model predictions. We found that the model detects 
                    aberrations in TP53, but it also picks up related biological processes associated with aggressive disease 
                    like lymph node metastasis and biochemical recurrence. Our results show that insights driven by molecular 
                    analysis enable a deeper understanding of such models by revealing both their strengths and limitations, 
                    thereby providing invaluable information for their adoption in practice.</p>
                </div>
                
                <div class="h-55 mt-2">
                    <img class="h-full w-full shadow-md object-cover rounded-xl" src="../assets/WSI_mut.jpg" alt="">
                </div>
            </div>
        </div>
        <div class="grid grid-cols-5">
            <div class=" md:col-span-1 col-span-5">
                <p class="list-info w-full">BIOCOMP `22</p>
            </div>
            <div class="md:col-span-4 col-span-5">
                <p>Self-supervised multimodel pre-training for lung adenocarcinoma overall survival prediction 
                    <button class="link">[pdf]</button> 
                    <button class="link"><a href="https://github.com/pacocp/SSL-Survival"> [code] </a></button>
                </p>
                <p class="pt-1 text-xs">Francisco Carrillo-Perez<sup>*</sup>, Marija Pizurica<sup>*</sup>, Ignacio Rojas, Kathleen Marchal, 
                                        Luis Javier Herrera and Olivier Gevaert
                </p>

                <button class="pt-1 text-xs" v-on:click="expanded_ssl = !expanded_ssl">{{expanded_ssl? '&#x21E1; hide' : '&#x21E2; show'}} abstract</button> 
                <div v-show="expanded_ssl" class="pt-1 text-xs abstract">
                    <p>
                        The collection of multiple modalities of cancer data has increased over the years, allowing research in complex problems such as cancer prognosis. However, given the high-dimensionality of biological data, efficiently training machine learning models when scarce samples are available is still challenging. In this work we propose a novel multimodal self-supervised learning framework based on neural networks for survival analysis and we evaluate it in a few-shot learning setting for lung adenocarcinoma prognosis. We show that the multimodal self-supervised pre-training is more effective than regular pre-training or training from scratch for two modalities (RNA-Seq and Whole Slide Imaging) when few samples are available. With the multimodal self-supervised learning framework, the relation between the modalities is learned in a pretext task and the leveraged information is successfully used for the relevant downstream task for both modalities, showing the potential of the proposed methodology.</p>
                </div>

                <div class="h-55 mt-2">
                    <img class="h-full w-full shadow-md object-cover rounded-xl" src="../assets/SSL_im.jpg" alt="">
                </div>
            </div>
        </div>
        <div class="grid grid-cols-5">
            <div class=" md:col-span-1 col-span-5">
                <p class="list-info w-full">AT4SSL `21</p>
            </div>
            <div class="md:col-span-4 col-span-5">
                <p>Frozen Pretrained Transformers for Neural Sign Language Translation 
                    <button class="link"><a href="https://aclanthology.org/2021.mtsummit-at4ssl.10.pdf"> [pdf] </a></button>
                    <button class="link"><a href="https://github.com/m-decoster/fpt4slt"> [code] </a></button>
                </p>
                <p class="pt-1 text-xs">Mathieu De Coster, Karel D'Oosterlinck, Marija Pizurica, Paloma Rabaey, Severine
                    Verlinden, Mieke Van Herreweghe, Joni Dambre</p>

                <button class="pt-1 text-xs" v-on:click="expanded_fpt = !expanded_fpt">{{expanded_fpt? '&#x21E1; hide' : '&#x21E2; show'}} abstract</button> 
                <div v-show="expanded_fpt" class="pt-1 text-xs abstract">
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
                expanded_fpt: false
            }
        }
}</script>

<style scoped>
.abstract{
    text-align: justify;
}    
</style>