# Rakuten-Pixel-Codes-for-Tracking-
Tracking Pixel Codes for Rakuten 


<!-- Rakutan Tracking Pixel --> <mvt:foreach iterator="charge" array="order:charges">
<mvt:if expr="l.settings:charge:type NE 'TAX' OR l.settings:charge:type NE 'SHIPPING'">
   <mvt:assign name="g.order_discount" value="'true'" />
</mvt:if>
</mvt:foreach>

<img src='https://track.linksynergy.com/ep?mid=42089&ord=&mvt:order:id;&skulist=<mvt:assign name="l.counter" value="0" /><mvt:foreach iterator="item" array="order:items"><mvt:assign name="l.counter" value="l.counter + 1" /><mvt:if expr="l.counter GT 1">|</mvt:if>&mvt:item:code;</mvt:foreach><mvt:if expr="g.order_discount EQ 'true'">|Discount</mvt:if>&qlist=<mvt:assign name="l.counter" value="0" /><mvt:foreach iterator="item" array="order:items"><mvt:assign name="l.counter" value="l.counter + 1" /><mvt:if expr="l.counter GT 1">|</mvt:if>&mvt:item:quantity;</mvt:foreach><mvt:if expr="g.order_discount EQ 'true'">|0</mvt:if>&amtlist=<mvt:assign name="l.counter" value="0" /><mvt:foreach iterator="item" array="order:items"><mvt:assign name="l.counter" value="l.counter + 1" /><mvt:if expr="l.counter GT 1">|</mvt:if><mvt:assign name="l.settings:item:price_pennies" value="l.settings:item:price * 100" />&mvt:item:price_pennies;</mvt:foreach><mvt:assign name="l.counter" value="0" /><mvt:foreach iterator="charge" array="order:charges"><mvt:if expr="l.settings:charge:type NE 'TAX' OR l.settings:charge:type NE 'SHIPPING'"><mvt:assign name="l.settings:charge:discount_pennies" value="l.settings:charge::formatted_disp_amt * 100" />|&mvt:charge:discount_pennies;</mvt:if></mvt:foreach>&cur=USD&namelist=<mvt:assign name="l.counter" value="0" /><mvt:foreach iterator="item" array="order:items"><mvt:assign name="l.counter" value="l.counter + 1" /><mvt:if expr="l.counter GT 1">|</mvt:if>&mvt:item:name;</mvt:foreach><mvt:if expr="g.order_discount EQ 'true'">|Discount</mvt:if>' border="0" width="1px" height="1px" alt="">
<!-- End Rakutan Tracking Pixel -->

