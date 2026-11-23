<script>
    let { flat } = $props();
</script>

<div class="offercard">
    <img src="./design/special-offers/assets/offer-{flat.id}.png" class="card-image" alt="flatImage"/>
    <div class="body-offercard">
        <p class="building">{flat.building}, {flat.floor}</p>
        <a href="#" class="">{flat.rooms} bedrooms, {flat.area} m²</a>
        <p class="aspect">aspect: {flat.aspect}</p>
        <div class="prices">
            <p class="offerprice"></p>
            <p class="listprice">£{flat.price}</p>
        </div>
        <a href="#" class="moreinfo"/>
    </div>
</div>

<style>
    .offercard {
        border: 1px solid #e2e8f0;
        border-radius: 8px;
        overflow: hidden;
        background: #fff;
    }
    .card-image {
        width: 100%;
        height: auto;
        display: block;
    }
    .body-offercard {
        padding: 16px;
    }
</style>