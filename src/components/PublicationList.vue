<template>
    <button class="mb-5 link tooltip"> <a href="https://scholar.google.com/citations?user=LrxvB8MAAAAJ&hl=en">[Google Scholar]</a></button>
    <div class="grid grid-cols-5">
            <div class=" md:col-span-1 col-span-5 text-lg">
                <p class="list-info w-full">Nature Biomedical Engineering `24</p>
            </div>
            <div class="md:col-span-4 col-span-5 text-lg">
                <p>RNA-to-image pan-cancer synthesis using cascaded diffusion models
                    <button class="link"><a href="https://www.biorxiv.org/content/10.1101/2023.01.13.523899v1">[paper link]</a></button>
                    <button class="link tooltip">[code]<span class="tooltiptext">coming soon!</span></button>
                </p>
                <p class="pt-1 text-sm">Francisco Carrillo-Perez, <span class="underline">Marija Pizurica</span>, Yuanning Zheng and Olivier Gevaert
                </p>

                <button class="pt-1 text-sm" v-on:click="expanded_e = !expanded_e">{{expanded_e? '&#x21E1; hide' : '&#x21E2; show'}} abstract</button> 
                <div v-show="expanded_e" class="pt-1 text-sm abstract">
                    <p>Synthetic data generation offers a solution to the data scarcity problem in biomedicine 
                        where data are often expensive or difficult to obtain. By increasing the dataset size, more powerful 
                        and generalizable machine learning models can be trained, improving their performance in clinical decision support systems. 
                        The generation of synthetic data for cancer diagnosis has been explored in the literature, but typically 
                        in the single modality setting (e.g. whole-slide image tiles or RNA-Seq data). 
                        Given the success of text-to-image synthesis models for natural images, where one modality is used to generate a 
                        related one, we propose RNA-to-image synthesis (RNA-CDM) in a multi-cancer context. 
                        First, we trained a variational auto-encoder in order to reduce the dimensions of the patient's gene expression profile, 
                        showing that this can accurately differentiate between different cancer types. 
                        Then, we trained a cascaded diffusion model to synthesize realistic whole-slide image tiles using the latent 
                        representation of the patient's RNA-Seq data. We show that generated tiles preserved the cell-type distribution 
                        found in real-world data, with important cell types detectable by a state-of-the-art cell identification model 
                        in the synthetic samples. Next, we successfully used this synthetic data to pretrain a multi-cancer classification model, 
                        observing an improvement in performance after training from scratch across 5-fold cross validation. 
                        Our results demonstrate the potential utility of synthetic data for developing multi-modal machine learning models 
                        in scarce data settings, as well as the possibility of imputing missing data modalitiesby leveraging 
                        the information present in available data modalities.</p>
                </div>
            </div>
        </div>
    <div class="flex flex-col space-y-5"> 
        <div class="grid grid-cols-5">
            <div class=" md:col-span-1 col-span-5 text-lg">
                <p class="list-info w-full"> Nature Machine Intelligence `23 </p>
            </div>
            <div class="md:col-span-4 col-span-5 text-lg">
                <p>Multimodal data fusion for cancer biomarker discovery with deep learning 
                    <button class="link"><a href="https://www.nature.com/articles/s42256-023-00633-5">[paper link]</a></button>
                </p>
                <p class="pt-1 text-sm"> Sandra Steyaert, <span class="underline">Marija Pizurica</span>, Priya Khandelwal Divya Nagaraj, 
                    Tina Hernandez-Boussard, Andrew J Gentles, and Olivier Gevaert  </p>

                <button class="pt-1 text-sm" v-on:click="expanded_s = !expanded_s">{{expanded_s? '&#x21E1; hide' : '&#x21E2; show'}} abstract</button> 

                <div v-show="expanded_s" class="pt-1 text-sm abstract">
                    <p>
                        Technological advances now make it possible to study a patient from multiple angles with high-dimensional, 
                        high-throughput multi-scale biomedical data. In oncology, massive amounts of data are being generated ranging 
                        from molecular, histopathology, radiology to clinical records. The introduction of deep learning has significantly 
                        advanced the analysis of biomedical data. However, most approaches focus on single data modalities leading to 
                        slow progress in methods to integrate complementary data types. Development of effective multimodal fusion 
                        approaches is becoming increasingly important as a single modality might not be consistent and sufficient 
                        to capture the heterogeneity of complex diseases to tailor medical care and improve personalised medicine. 
                        Many initiatives now focus on integrating these disparate modalities to unravel the biological processes 
                        involved in multifactorial diseases such as cancer. However, many obstacles remain, including lack of usable 
                        data as well as methods for clinical validation and interpretation. Here, we cover these current challenges 
                        and reflect on opportunities through deep learning to tackle data sparsity and scarcity, multimodal 
                        interpretability, and standardisation of datasets.
                        </p>
                </div>
            </div>
        </div>
        <div class="grid grid-cols-5">
            <div class=" md:col-span-1 col-span-5 text-lg">
                <p class="list-info w-full"> Cancer Research `23 </p>
            </div>
            <div class="md:col-span-4 col-span-5 text-lg">
                <p>Whole slide imaging-based prediction of <span class='italic'>TP53</span> mutations identifies an aggressive disease phenotype in prostate cancer   
                    <button class="link"><a href="https://aacrjournals.org/cancerres/article/doi/10.1158/0008-5472.CAN-22-3113/727461/Whole-slide-imaging-based-prediction-of-TP53">[paper link]</a></button>
                    <button class="link"><a href="https://github.com/mpizurica/WSI_mut">[code]</a></button>
                </p>
                <p class="pt-1 text-sm"> <span class="underline">Marija Pizurica</span>, Maarten Larmuseau, Kim Van der Eecken, 
                     Louise de Schaetzen van Brienen, Francisco Carrillo-Perez, Simon Isphording, Nicolaas Lumen, Jo Van Dorpe, 
                     Piet Ost, Sofie Verbeke, Olivier Gevaert<sup>*</sup> 
                     and Kathleen Marchal<sup>*</sup></p>

                <button class="pt-1 text-sm" v-on:click="expanded = !expanded">{{expanded? '&#x21E1; hide' : '&#x21E2; show'}} abstract</button> 

                <div v-show="expanded" class="pt-1 text-sm abstract">
                    <p>
                        In prostate cancer, there is an urgent need for objective prognostic biomarkers that identify the metastatic 
                        potential of a tumor at an early stage. While recent analyses indicated <span class='italic'>TP53</span> mutations as candidate biomarkers, 
                        molecular profiling in a clinical setting is complicated by tumor heterogeneity. Deep learning models that predict 
                        the spatial presence of <span class='italic'>TP53</span> mutations in whole slide images (WSIs) offer the potential to mitigate this issue. 
                        To assess the potential of WSIs as proxies for spatially resolved profiling and as biomarkers for aggressive disease, 
                        we developed <span class='italic'>TiDo</span>, a deep learning model that achieves state-of-the-art performance in predicting <span class='italic'>TP53</span> mutations 
                        from WSIs of primary prostate tumors. In an independent multi-focal cohort, the model showed successful 
                        generalization at both the patient and lesion level. Analysis of model predictions revealed that false positive (FP)
                        predictions could at least partially be explained by <span class='italic'>TP53</span> deletions, suggesting that some FP carry an alteration 
                        that leads to the same histological phenotype as <span class='italic'>TP53</span> mutations. Comparative expression and histological cell 
                        type analyses identified a <span class='italic'>TP53</span>-like cellular phenotype triggered by expression of pathways affecting stromal 
                        composition. Together, these findings indicate that WSI-based models might not be able to perfectly predict the 
                        spatial presence of individual <span class='italic'>TP53</span> mutations but they have the potential to elucidate the prognosis of a tumor 
                        by depicting a downstream phenotype associated with aggressive disease biomarkers.
                        </p>
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
                    <button class="link tooltip">[paper link]<span class="tooltiptext">coming soon!</span></button>
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
                <p class="list-info w-full">Cell Reports Methods `23</p>
            </div>
            <div class="md:col-span-4 col-span-5 text-lg">
                <p>Synthetic whole-slide image tile generation with gene expression profiles infused deep generative models
                    <button class="link"><a href="https://www.cell.com/cell-reports-methods/pdfExtended/S2667-2375(23)00171-6">[paper link]</a></button>
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
            </div>
        </div>
        
        <div class="grid grid-cols-5">
            <div class=" md:col-span-1 col-span-5 text-lg">
                <p class="list-info w-full">Nature Communications `23</p>
            </div>
            <div class="md:col-span-4 col-span-5 text-lg">
                <p>Spatial Cellular Architecture Predicts Prognosis in Glioblastoma
                    <button class="link"><a href="https://www.nature.com/articles/s41467-023-39933-0">[paper link]</a></button>
                    <button class="link"><a href="https://github.com/gevaertlab/GBM360">[code]</a></button>
                </p>
                <p class="pt-1 text-sm"> Yuanning Zheng, Francisco Carrillo-Perez, <span class="underline">Marija Pizurica</span>, Dieter Henrik Heiland and Olivier Gevaert
                </p>

                <button class="pt-1 text-sm" v-on:click="expanded_diff = !expanded_diff">{{expanded_diff? '&#x21E1; hide' : '&#x21E2; show'}} abstract</button> 
                <div v-show="expanded_diff" class="pt-1 text-sm abstract">
                    <p>	Intra-tumoral heterogeneity and cell-state plasticity are key drivers for the therapeutic resistance of glioblastoma (GBM). Studies based on single-cell RNA-seq and spatial transcriptomics have classified GBM cells into distinct transcriptional phenotypes. However, how the transcriptional diversity and spatial cellular organization are associated with patient prognosis remains incompletely resolved. Here, we developed a deep learning model to predict spatially resolved transcriptional programs from histology images. The model was trained on spatial transcriptomics data and validated in external testing cohorts. Applying the model to two separate patient cohorts led to the discovery of conserved relationships between tumor architecture and prognosis. Patients with poor prognosis had higher proportions of GBM cells expressing a hypoxia-induced transcriptional program. In addition, a clustering pattern of reactive astrocytes contributed to a poor prognosis. Conversely, when the reactive astrocytes were dispersed and connected to other cell types, the risk was decreased. To validate our results, we developed a separate deep learning model that used histology images to predict prognosis. Applying the model to spatial transcriptomics data discovered survival-associated regional gene expression programs. Genes related to glycoprotein metabolism and injury response were significantly upregulated in tumor cells with higher aggressiveness. Our studies established a scalable approach to resolve the transcriptional heterogeneity of GBM and linked the spatial cellular architecture to clinical outcomes.</p>
                </div>
            </div>
        </div>
        <div class="grid grid-cols-5">
            <div class=" md:col-span-1 col-span-5 text-lg">
                <p class="list-info w-full">AT4SSL `21</p>
            </div>
            <div class="md:col-span-4 col-span-5 text-lg">
                <p>Frozen Pretrained Transformers for Neural Sign Language Translation 
                    <button class="link"><a href="https://aclanthology.org/2021.mtsummit-at4ssl.10.pdf"> [paper link] </a></button>
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
                expanded_s: false,
                expanded: false,
                expanded_ssl: false,
                expanded_fpt: false,
                expanded_rna_gan: false,
                expanded_diff: false,
                expanded_e: false,

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