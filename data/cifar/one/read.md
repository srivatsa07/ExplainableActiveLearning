final_model_cifar, cifar_aggregate, cifar_per_image = xal_with_visuals(
    dataset=cifar_train_subset,
    model=cifar_model,
    mean=IMAGENET_MEAN,
    std=IMAGENET_STD,
    init_size=2000,
    query_size=100,
    n_cycles=20,
    batch_size=1100,
    workers=20,
    val_loader=cifar_val_loader,
    test_loader=cifar_test_loader,
    threshold=0.9,
    dataset_name="cifar10",
    xai_image_size=100,
    tracking_subset=cifar_tracking_subset


##         correctness_metric = PixelFlipping(
            perturb_baseline="black",    # Mask important pixels with black (zero)
            features_in_step=224,         # Number of pixels/features to mask per step (adjust as needed) 2,4,8,16,32,64,112,224
            normalise=True               # Normalize attributions before ranking
        )

##     img_pil = img_pil.rotate(15)  # 15° rotation for natural images
