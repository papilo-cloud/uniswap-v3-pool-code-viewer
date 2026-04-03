# UniswapV3Pool — Annotated Code Viewer

An interactive, fully annotated deep-dive into `UniswapV3Pool.sol`. Click any section in the code to see a detailed explanation of the design decisions, math, gas optimisations, and security patterns behind it.

**[Open the viewer](https://github.com/papilo-cloud/uniswap-v3-pool-code-viewer)**

---

## What's covered

19 annotated sections spanning the full contract:

- `Slot0` — single-slot packing of price, tick, oracle pointer, and reentrancy lock
- `feeGrowthGlobal` — Q128.128 per-unit-liquidity fee accumulators
- `ticks` & `tickBitmap` — liquidityNet, feeGrowthOutside, and bitmap bit-scanning
- `mint()` / `burn()` / `collect()` — the liquidity lifecycle
- `swap()` — the tick-crossing loop, fee split, oracle write, and callback pattern
- `flash()` — uncollateralized loans with fee verification
- `observe()` / `snapshotCumulativesInside()` — TWAP oracle queries
- `setFeeProtocol()` / `collectProtocol()` — governance fee switch

---

## Local preview

No build step. Just open `index.html` in a browser.

```bash
open index.html
```