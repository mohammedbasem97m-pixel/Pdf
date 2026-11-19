<!-- علم العراق المتحرك في الزاوية -->
<div class="iraq-flag-corner" title="العراق">
  <div class="flag-wave">
    <div class="stripe red"></div>
    <div class="stripe white">
      <span class="takbir">الله أكبر</span>
    </div>
    <div class="stripe black"></div>
    <div class="gloss"></div>
  </div>
</div>

<style>
  .iraq-flag-corner {
    position: fixed;
    top: 15px;      /* المسافة من الأعلى */
    left: 15px;     /* المسافة من اليسار (غيرها إلى right: 15px إذا أردته في الزاوية اليمنى) */
    z-index: 9999;
    perspective: 400px;
  }

  .flag-wave {
    width: 75px;
    height: 50px;
    border-radius: 4px;
    overflow: hidden;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.25);
    display: flex;
    flex-direction: column;
    position: relative;
    transform-origin: left center;
    animation: waveFlag 2.5s ease-in-out infinite alternate;
  }

  .stripe {
    flex: 1;
    width: 100%;
  }

  .stripe.red {
    background-color: #ce1126;
  }

  .stripe.white {
    background-color: #ffffff;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .stripe.black {
    background-color: #000000;
  }

  .takbir {
    color: #007a3d;
    font-family: 'Tahoma', 'Arial', sans-serif;
    font-size: 11px;
    font-weight: bold;
    line-height: 1;
    letter-spacing: 0.5px;
  }

  /* تأثير التموج واللمعان */
  .gloss {
    position: absolute;
    inset: 0;
    background: linear-gradient(
      110deg,
      rgba(255, 255, 255, 0) 20%,
      rgba(255, 255, 255, 0.35) 45%,
      rgba(0, 0, 0, 0.15) 65%,
      rgba(255, 255, 255, 0) 85%
    );
    background-size: 200% 100%;
    animation: shimmerWave 2.5s ease-in-out infinite alternate;
    pointer-events: none;
  }

  @keyframes waveFlag {
    0% {
      transform: rotateY(-8deg) skewY(-2deg);
    }
    50% {
      transform: rotateY(8deg) skewY(2deg);
    }
    100% {
      transform: rotateY(-5deg) skewY(-1deg);
    }
  }

  @keyframes shimmerWave {
    0% {
      background-position: 100% 0;
    }
    100% {
      background-position: 0% 0;
    }
  }
</style>
