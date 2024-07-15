<script lang="ts">
    import { PrivateKey } from '@bsv/sdk'
    
    let WIF:string
    let address:string
    
    function createKeys () {
    
        const privKey = PrivateKey.fromRandom()
        WIF = privKey.toWif()
        console.log("Private Key WIF format is ", WIF)
        address = privKey.toAddress()
        console.log("Your bitcoin address is ", address)
    }
    
    </script>
    
    <section style="margin-left: 400px; margin-top: 200px; margin-right: 20px; margin-bottom: 20px;">
        
        <p>Private Key WIF format is <b>{WIF}</b></p>
        <p>Your BitCoin Address is <b>{address}</b></p> 
        <button class=" bg-black text-white p-2 rounded mx-auto " on:click={createKeys}> Generate New Wallet Keys </button>
    </section>
    
    