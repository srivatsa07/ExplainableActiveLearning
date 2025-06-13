# Run active learning
final_model_pcam,pcam_aggregate, pcam_per_image = xal_with_pcam(
    dataset=pcam_train_subset,
    model=pcam_model,
    mean=IMAGENET_MEAN,
    std=IMAGENET_STD,
    init_size=2000,
    query_size=100,
    n_cycles=20,
    batch_size=1200,
    workers=10,
    val_loader=pcam_val_loader,
    test_loader=pcam_test_loader,
    recall_threshold=0.95,
    dataset_name="pcam",    
    xai_image_size=100,
    tracking_subset=pcam_tracking_subset
)



##         correctness_metric = PixelFlipping(
            perturb_baseline="black",    # Mask important pixels with black (zero)
            features_in_step=224,         # Number of pixels/features to mask per step (adjust as needed) 2,4,8,16,32,64,112,224
            normalise=True               # Normalize attributions before ranking
        )

## CONTINUITY
        perturb_func = quantus.gaussian_noise
        perturb_kwargs = {"std": 0.05}