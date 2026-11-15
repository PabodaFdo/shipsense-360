# ShipSense 360 Risk Register

| ID | What could go wrong | Why it matters | How to reduce the risk | Status |
|---|---|---|---|---|
| R-01 | An order with several items is counted more than once. | The dashboard could overstate order volume and report misleading late-shipping rates. | Count each eligible order once. Test with an order that has multiple items. | Open |
| R-02 | The model uses information recorded after an order is placed. | The model could score well on historical data and still fail to score new orders reliably. | Document when each input becomes available. Use only inputs available when the order is placed. | Open |