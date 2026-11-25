<script>
    let { flat } = $props();
    let offerPrice = $derived(Math.ceil(flat.price * 0.93 / 100) * 100);

</script>

<div class="offercard">
    <img 
        src="./design/special-offers/assets/offer-{flat.id}.png"
        class="card-image" 
        alt="flatImage"
        onerror={(error) => {
            error.currentTarget.onerror = null;
            error.currentTarget.src = './design/special-offers/assets/default-image.png';
        }}
    />
    <div class="body-offercard">
        <p class="building">Address: {flat.building}, {flat.floor}</p>
        <a href="#" class="square">{flat.rooms} bedrooms, {flat.area} m²</a>
        <p class="aspect">{flat.aspect}</p>
        <div class="prices">
            <p class="offerprice">Offer price: £{offerPrice}</p>
            <p class="listprice">List price: £{flat.price}</p>
        </div>
        <a href="#" class="more-info">Book a view</a>
    </div>
</div>

<style>
    .offercard {
        width: 100%;
        height: 100%;
        border: 1px solid black;
        border-radius: 8px;
        overflow: hidden;
        background: #fff;
    }
    
    .card-image {
        width: 100%;
        aspect-ratio: 1/1;
        object-fit: fill;
        height: auto;
        display: block;
    }

    .body-offercard {
        border-top: 1px solid black;
        padding: 16px;
    }

    .building {
        font-size: var(--step-body);
        color: var(--muted);
    }

    .square {
        color: var(--ink);
    }

    .aspect {
        color: var(--muted);
        font-size: var(--step-body);
    }

    .prices {
        font-family: var(--font);
    }

    .more-info {
        text-decoration: underline !important;
        color: var(--ink);
    }
</style>