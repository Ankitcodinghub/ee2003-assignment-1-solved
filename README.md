# ee2003-assignment-1-solved
**TO GET THIS SOLUTION VISIT:** [EE2003 # Assignment 1 Solved](https://www.ankitcodinghub.com/product/ee2003-assignment-1-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;90767&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;5&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (5 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EE2003 # Assignment 1 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (5 votes)    </div>
    </div>
# Assignment 1

This assignment deals with implementation of a sequential multiplier in Verilog HDL.

## Goals

– Demonstrate basic working knowledge of verilog

– Practice git

– Practice assignment submission and feedback

## Given

– Test bench for sequential divider

– Template code that you can use to fill in

– Some test cases

## Details on the assignment

### Multiplication

This basically refers to the “long form” multiplication as we learn in school. For each digit of the multiplier, we shift the multiplicand to the appropriate place value, and then add all the partial products. An example of the partial products in binary for a simple 4-bit multiplication are shown below. As expected, multiplying two 4-bit numbers can result in an output that is up to 8 bits in length.

“`

0110 # Decimal 6 – Multiplicand

x 0011 # Decimal 3 – Multiplier

——–

0110 # Partial product 0 (PP0)

0110 # PP1

0000 # PP2

0000 # PP3

——–

00010010 # Decimal 18

——–

“`

### Number representation

The numbers themselves are represented in 2’s complement notation. Therefore, if the multiplicand is negative, the PP values should be “sign-extended” to get the correct result. An example for negative multiplicand is shown below – negative multiplier requires similar careful handling, and is left as an exercise.

“`

1010 # Decimal -6

x 0011 # Decimal 3

——–

11111010 # Partial product 0 (PP0) – sign extended

1111010 # PP1

000000 # PP2

00000 # PP3

——–

(1)11101110 # Decimal -18 (discard the overflow 1)

——–

“`

### Hardware implementation

The above multiplication process can be directly implemented as combinational logic, where each partial product vector is created using a set of AND gates, and the results are put through a chain of adders.

The other alternative is to have a reduced hardware with a single register to hold the final product. This **accumulates** the final product by iterating over several clock cycles (how many?). A diagram indicating the architecture is shown here.

![Sequential Multiplier](./fig/seqmult.png)
