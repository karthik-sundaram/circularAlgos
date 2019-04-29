
# Functionalities of this package:

- <b>r_vonmises()</b>     : This function is used for generating random numbers for a von Mises circular distribution
- <b>q_vonmises()</b>     : This function is used used to calculate the quantiles for the given probabilities for a von Mises distribution
- <b>p_vonmises()</b>     : This function is  used to calculate the CDF value at the given points for a von Mises distribution
- <b>d_vonmises()</b>     : This function is for calculating the PDF at the given points for a von Mises circular distribution
- <b>angles_VMF_mix()</b> : This function is used to fit angular data in radians using the expectation maximization algorithm for maximum likelihood estimatation of the parameters of the different mixtures
- <b>vmf_clust()</b>      : This function is used to:  
    - fit the given data using the expectation maximization algorithm for maximum likelihood estimatation of the parameters of the different mixtures
    - Perform probabilistic clustering using the mixtures obtained above


```python

```

# Installation Instructions:

### option (a)


```python
pip install circular_algos
```

### option (b)


```python
pip install git+git://github.com/karthik-sundaram/circular_algos.git
```


```python

```

# Example


```python
from circular_algos import circular_stat
```

## r_vonmises()

- <b>Parameters:</b>
    - n: int, Number of observations
    - mu: float/int, location parameter
    - kappa: float/int, scale parameter. Large values of kappa corresponds to lower variance
- <b>Returns:</b>
    - rv_ls: list, pdf function
    - <plot>: plot of random numbers


```python
circular_stat.r_vonmises(1000,1,1)
```




    (array([8.45968334e-01, 1.61992822e+00, 1.97694438e+00, 1.81044062e+00,
            5.54721521e+00, 8.10438636e-01, 3.05647073e+00, 6.25305161e+00,
            5.22989526e+00, 2.98012240e+00, 2.06101481e+00, 1.19279137e+00,
            4.37581486e+00, 1.09588218e+00, 5.05762969e+00, 5.33442496e+00,
            4.19550431e+00, 1.03879854e-01, 2.80263162e+00, 6.27846524e+00,
            1.80056673e+00, 1.59960234e+00, 6.07149624e+00, 9.74595200e-01,
            2.49113314e+00, 8.82694169e-01, 2.80842695e+00, 3.43775115e+00,
            1.78522020e+00, 4.05000865e+00, 6.96232887e-01, 8.46655416e-01,
            1.10541965e+00, 5.87455861e+00, 4.92731963e+00, 1.56781722e+00,
            1.11933559e+00, 3.11846833e+00, 5.84667085e+00, 8.56098616e-01,
            6.10505058e+00, 6.17115088e+00, 1.95795756e+00, 4.22751657e+00,
            4.94061891e+00, 3.35974046e-02, 6.11463226e+00, 1.47247991e-01,
            6.43726838e-01, 5.31214310e+00, 9.68568885e-01, 1.60294588e+00,
            5.14731478e+00, 3.15515163e+00, 1.10011594e+00, 1.59074121e+00,
            1.21628549e+00, 3.35941560e+00, 1.56621145e+00, 4.13146327e-01,
            1.84892432e+00, 2.47597303e+00, 3.49143986e+00, 2.96828233e+00,
            3.17719248e+00, 1.40557723e+00, 1.16510777e+00, 1.26876823e+00,
            2.57374031e+00, 9.84670332e-02, 5.14252886e+00, 1.15539608e+00,
            6.26011699e+00, 2.26488813e+00, 5.52224477e+00, 1.48003636e+00,
            5.63610137e+00, 1.06907729e+00, 9.79791313e-02, 5.80764632e-01,
            2.69643043e+00, 1.99575696e-01, 4.78617590e+00, 1.95506465e+00,
            3.78916989e+00, 9.34115201e-01, 1.11547666e+00, 7.68281837e-01,
            1.07255580e+00, 3.12699779e+00, 7.98331283e-01, 5.87737116e-01,
            1.70431776e+00, 8.36778885e-02, 2.10241908e+00, 8.51989803e-01,
            7.64340544e-01, 1.53698483e+00, 4.93949970e+00, 7.56517519e-01,
            9.86187501e-01, 1.01815777e+00, 8.84982859e-01, 1.13002572e+00,
            6.06980453e+00, 3.31488958e-02, 6.66198721e-01, 6.00379483e+00,
            1.68129237e-01, 5.01137164e+00, 7.37369668e-01, 3.97903963e+00,
            8.97008467e-01, 2.01977806e+00, 1.66752174e+00, 2.38615371e-01,
            2.07217778e-01, 1.38584132e+00, 3.58952377e+00, 7.49906671e-01,
            1.34405585e+00, 7.98553142e-01, 5.06547368e-01, 1.89280917e+00,
            2.17067073e+00, 4.19058854e-01, 6.05276428e+00, 2.11743587e+00,
            1.81024006e+00, 2.17714962e+00, 3.89709722e+00, 1.39701051e+00,
            9.09257624e-01, 1.07187587e+00, 1.16887527e+00, 1.38489204e+00,
            9.71943499e-01, 5.65327543e+00, 5.93699661e+00, 7.07081735e-01,
            5.21504825e-02, 5.92446612e+00, 3.74567439e+00, 4.38506304e+00,
            1.54135296e+00, 4.72565237e-01, 8.26236084e-01, 5.82624792e+00,
            1.76408934e+00, 1.81283894e+00, 5.78081706e+00, 1.39211910e+00,
            3.04476401e+00, 3.99686015e-01, 1.26105415e+00, 2.10743068e+00,
            3.52839877e+00, 7.47777893e-01, 2.69659135e-01, 1.18850516e+00,
            6.07752872e+00, 1.51185379e+00, 5.84898569e-01, 1.48143146e+00,
            3.19495573e+00, 1.66317885e+00, 1.99404472e+00, 3.07777109e+00,
            1.02695321e+00, 6.58688055e-01, 5.76470125e+00, 5.78383970e+00,
            1.58481890e+00, 4.10165298e+00, 1.37559688e-01, 1.19894488e+00,
            1.40952845e+00, 1.53965705e+00, 5.63449039e-01, 2.38239758e+00,
            4.91974023e+00, 6.47758334e-01, 1.48738151e+00, 6.30969733e-01,
            1.18013608e+00, 5.17913133e+00, 1.64285394e+00, 6.16518273e+00,
            8.06307612e-01, 1.62071750e+00, 7.42391861e-01, 1.78986355e-01,
            1.85268853e+00, 9.09427053e-01, 5.64596957e+00, 5.17302446e+00,
            6.79769543e-01, 9.62772386e-01, 1.59408592e+00, 5.29560466e+00,
            5.88242030e+00, 6.24468320e+00, 2.18674857e+00, 5.46874697e+00,
            3.40170665e+00, 2.11082834e+00, 1.80698261e+00, 8.28219247e-01,
            3.51742423e+00, 4.83353301e-02, 6.26692413e-01, 5.30071805e+00,
            1.57954299e+00, 7.25857602e-01, 3.09709204e-02, 2.07788309e+00,
            4.60623801e+00, 1.08734719e+00, 3.05316942e+00, 8.11450501e-01,
            2.20816820e+00, 8.48734491e-01, 1.65613522e+00, 2.49135192e+00,
            9.99654095e-01, 2.79647156e+00, 6.10523110e-01, 1.05737135e+00,
            6.17731463e+00, 4.09800386e-01, 1.78291771e+00, 1.31350306e+00,
            1.74856564e+00, 3.77878699e+00, 6.07386237e+00, 5.36036899e-01,
            6.67153754e-01, 1.41488533e+00, 2.76728968e+00, 4.61455833e+00,
            5.30116220e+00, 1.90171373e+00, 3.45630239e+00, 1.50875426e+00,
            1.29722279e+00, 1.33212900e+00, 3.86050441e+00, 1.77097591e+00,
            6.04039640e+00, 8.45057744e-01, 1.90314060e+00, 3.80308348e-01,
            5.66825705e+00, 2.32307133e+00, 1.07465697e+00, 1.72675867e+00,
            2.07602791e+00, 1.49487813e+00, 2.44911373e+00, 3.22503087e+00,
            5.78704831e-01, 8.85962377e-01, 9.98124701e-01, 5.77655598e+00,
            1.00729190e-01, 2.66620924e+00, 2.59167984e+00, 6.95859370e-01,
            1.90399600e+00, 2.65911301e+00, 6.05296146e+00, 4.58299798e+00,
            6.40412196e-01, 4.10414624e+00, 1.37806215e+00, 2.45983985e-01,
            1.68910203e+00, 4.07735733e+00, 1.40027166e+00, 1.03423569e-01,
            4.73969052e+00, 4.30208792e+00, 3.68256561e+00, 1.92345551e+00,
            7.51837456e-01, 1.20962916e+00, 8.99140733e-01, 6.22693058e+00,
            6.28225043e+00, 1.79187255e+00, 9.51923636e-01, 5.51903782e-01,
            1.87966157e+00, 7.74645426e-02, 1.39383432e+00, 1.87512846e+00,
            2.61072249e+00, 4.56349210e-01, 1.91456464e+00, 8.96580131e-01,
            4.71328629e-01, 6.73818646e-02, 9.97419633e-01, 6.25812509e+00,
            2.27444401e+00, 7.65295437e-01, 1.43223494e-01, 9.79684080e-01,
            2.75796816e+00, 3.46423808e-03, 5.95939006e-01, 6.87206293e-01,
            1.60041311e+00, 1.03927660e+00, 5.88068935e+00, 5.57244374e-01,
            1.54780961e+00, 1.18356349e+00, 1.11447157e+00, 2.54440194e+00,
            6.13039871e+00, 5.28714823e-01, 4.44639345e+00, 1.95446129e+00,
            2.05421544e+00, 8.76532577e-01, 1.24183911e+00, 1.86637405e+00,
            6.89275432e-01, 4.11107170e+00, 7.20048537e-01, 6.24147210e+00,
            5.94235672e+00, 5.80071029e+00, 1.51633090e+00, 3.87526163e+00,
            1.28578746e+00, 1.26915793e+00, 5.17905168e-01, 1.60290823e+00,
            1.67403822e+00, 7.58274195e-01, 1.86865168e+00, 5.71600651e-01,
            5.00710040e+00, 2.77946270e+00, 1.04190287e+00, 2.34064488e+00,
            2.27311194e+00, 5.67906997e+00, 2.07767407e+00, 3.42862524e+00,
            1.45705336e+00, 3.53512339e-01, 2.71407754e+00, 5.50219026e+00,
            2.57917042e-01, 1.00811825e+00, 5.73858041e+00, 1.38236223e+00,
            1.57723218e+00, 6.49841477e-01, 1.01351956e+00, 2.78059558e-01,
            8.95859421e-01, 8.05853179e-01, 1.27769000e+00, 3.45208029e+00,
            5.92119860e+00, 3.21210211e+00, 3.08800479e+00, 1.24261026e+00,
            6.42724084e-01, 4.39425099e-02, 5.29524948e+00, 5.34238278e-01,
            3.24645792e-01, 5.58625900e+00, 7.70481977e-01, 5.97938676e+00,
            1.85708865e+00, 1.65133629e+00, 5.62546522e-01, 1.68754865e+00,
            1.34870737e+00, 1.59632250e+00, 6.16364083e+00, 1.06190612e-01,
            1.27727792e-01, 8.84486363e-01, 6.45662481e-01, 1.14333907e-01,
            4.03181558e+00, 1.36658396e+00, 2.34048075e+00, 1.97335395e+00,
            1.52778898e+00, 1.75321074e+00, 3.98480257e+00, 3.13807066e-01,
            1.08316502e+00, 6.25038596e-02, 6.18838744e+00, 1.84787070e+00,
            5.06183436e+00, 2.79774162e+00, 1.19792972e+00, 2.13726645e+00,
            1.96752059e+00, 2.46560327e+00, 3.12338650e+00, 1.69251259e+00,
            6.04839801e-01, 1.35937933e+00, 5.63397992e+00, 2.86850024e+00,
            5.76865480e+00, 8.41180469e-01, 7.10975020e-01, 6.81958715e-01,
            5.95228857e-01, 1.28112555e+00, 1.06553237e+00, 2.75230307e+00,
            1.41759965e+00, 1.85709055e+00, 1.51614724e+00, 5.70903450e-02,
            8.65614779e-01, 1.31758230e+00, 1.09298667e-01, 5.45635696e+00,
            2.65985138e-01, 7.87542597e-01, 6.19790169e+00, 2.29080929e-01,
            7.11088234e-01, 1.14134833e-01, 1.09987656e+00, 1.88759785e+00,
            1.90578370e+00, 1.12567355e-01, 6.13803178e+00, 3.26990856e+00,
            1.43354052e+00, 1.46134404e+00, 6.05807988e+00, 3.99853897e+00,
            5.95521342e+00, 4.88256043e-01, 5.96162989e+00, 7.75591394e-01,
            1.21959162e+00, 4.72435315e-01, 1.56373320e+00, 1.29678992e+00,
            5.08671536e+00, 5.04102695e+00, 1.64676050e+00, 6.92002901e-01,
            6.00604034e+00, 1.38522144e+00, 4.23714704e+00, 5.72785842e+00,
            2.82931418e+00, 1.19999589e+00, 4.29621470e-02, 3.61284392e+00,
            2.42725702e+00, 5.45561062e+00, 5.78386540e+00, 9.05268033e-01,
            1.00115798e-01, 5.45472056e+00, 1.76912735e+00, 2.23599875e+00,
            2.27070605e+00, 5.43118896e+00, 5.01706751e+00, 9.34323927e-01,
            6.21678887e+00, 2.07480478e+00, 5.54047334e+00, 6.15476782e+00,
            2.00531917e+00, 1.57072255e+00, 3.09336917e+00, 7.24878532e-02,
            1.89082596e+00, 2.13795138e+00, 1.29860695e+00, 2.83633871e+00,
            3.31450028e+00, 6.26705613e+00, 1.00521417e-01, 5.43429986e+00,
            2.10202513e+00, 2.34067143e+00, 3.36804274e+00, 5.76437474e+00,
            4.02335753e-01, 5.94329707e-01, 1.49880660e+00, 2.44461444e+00,
            2.34550159e+00, 5.62145156e+00, 1.31992719e+00, 3.14652131e+00,
            1.72212935e+00, 1.32528752e+00, 2.58748657e+00, 1.29557534e-01,
            5.84338703e-01, 3.46185371e+00, 2.37436164e+00, 2.32502215e+00,
            1.73088693e+00, 5.82875355e+00, 4.78316284e-01, 7.73982904e-01,
            2.95779690e-02, 4.91729840e+00, 4.88469863e-01, 2.24124973e+00,
            3.86767649e+00, 3.48367117e-01, 8.44380186e-01, 8.13403654e-01,
            8.99870442e-01, 6.06192920e-01, 2.44195665e+00, 5.39654283e-01,
            1.24271599e+00, 4.37109133e+00, 8.82636244e-01, 1.48302741e+00,
            2.70952642e-01, 1.51275726e+00, 1.11750715e+00, 5.55927129e+00,
            4.80017357e+00, 6.59428015e-01, 2.62504867e-01, 2.10392867e-01,
            6.55055515e-01, 3.77531087e+00, 9.45171356e-01, 2.70113221e+00,
            4.70629500e+00, 5.84745320e+00, 1.56453482e+00, 1.30827449e+00,
            2.76461388e-01, 3.46106344e-02, 1.46533716e-01, 2.00377741e-01,
            8.54639805e-01, 1.40078420e+00, 3.82140023e+00, 1.37681334e-01,
            4.91553694e-01, 5.50664345e+00, 2.14322923e-01, 5.23322916e+00,
            2.17443935e+00, 1.59298855e+00, 6.04323255e+00, 1.02278626e+00,
            1.34872168e+00, 8.33059814e-01, 2.03390614e+00, 1.68564159e+00,
            2.57034289e+00, 5.15277436e+00, 6.49559063e-01, 2.65244032e+00,
            5.49937269e+00, 3.89093867e+00, 2.97912522e+00, 9.58303272e-01,
            4.29331899e+00, 5.86217772e-01, 2.32594291e+00, 3.85251914e-01,
            1.78680239e+00, 1.33385488e+00, 3.69699977e-01, 3.06704423e+00,
            2.95850772e+00, 1.91080626e+00, 2.05840958e+00, 3.21360583e+00,
            5.56565403e+00, 2.44484086e+00, 5.84574318e+00, 1.32066991e+00,
            1.03413284e-01, 6.19869308e+00, 1.33368089e+00, 2.85656101e+00,
            1.31649868e+00, 2.21509911e+00, 1.86351132e+00, 2.60499761e-01,
            1.40802928e+00, 5.84570489e+00, 5.09018309e+00, 7.55885404e-01,
            3.18676780e-01, 2.96221616e-01, 4.14688881e-01, 9.56142628e-01,
            5.26621841e+00, 2.44679802e+00, 3.35611790e+00, 1.82910235e+00,
            5.29456711e-01, 4.31334888e-01, 1.08160065e+00, 2.47074567e+00,
            3.52030187e-01, 1.14222893e+00, 5.68265360e+00, 1.39592194e+00,
            6.13508819e+00, 1.64035577e+00, 5.03735879e+00, 1.48197944e+00,
            6.10811708e+00, 1.68578267e+00, 3.44652521e-02, 1.53062130e+00,
            1.22611946e+00, 3.51421784e-01, 1.50128822e+00, 1.29300767e-02,
            7.88785121e-01, 2.43892721e+00, 2.76883972e+00, 2.35467579e+00,
            1.55653747e+00, 3.47869427e+00, 1.18825625e+00, 1.96481060e+00,
            2.33679170e+00, 2.81226766e-01, 6.63567398e-01, 2.99623808e+00,
            1.51239215e+00, 3.59252332e-01, 2.23458834e+00, 2.20477784e+00,
            1.20768839e+00, 8.01941892e-01, 1.13984709e+00, 1.86411348e+00,
            1.61398701e+00, 2.57170403e-01, 6.01743916e+00, 2.48432548e+00,
            5.14452009e+00, 6.18004871e+00, 1.44666305e+00, 1.28628988e+00,
            1.55508465e+00, 1.76472567e-01, 2.14904416e+00, 6.17668132e+00,
            3.28969351e-01, 8.67858145e-01, 1.74402987e+00, 1.90382729e+00,
            6.10810830e+00, 1.33541890e+00, 2.06435183e+00, 3.04812057e+00,
            1.38115892e+00, 1.29178611e+00, 1.44594680e+00, 2.53257208e+00,
            9.21893380e-01, 3.00263717e-01, 7.80860087e-01, 5.80626079e+00,
            3.34866118e-01, 4.51334133e+00, 4.76303423e-01, 2.29808333e+00,
            1.88955897e-01, 1.52859434e+00, 1.63569316e+00, 1.66635814e+00,
            3.10657387e+00, 5.30375217e+00, 1.34957535e+00, 5.36860673e-02,
            2.89157474e+00, 1.00067728e+00, 1.38231730e+00, 1.55072680e+00,
            6.59639676e-01, 6.04434958e-01, 1.76145770e+00, 1.21351638e+00,
            6.36188700e-01, 1.02380577e+00, 7.08178413e-01, 6.11372797e+00,
            1.41245907e+00, 1.21332706e+00, 2.45184790e+00, 3.88394705e+00,
            2.88506960e+00, 2.09229417e+00, 1.38806831e+00, 2.49056584e+00,
            1.90573840e+00, 1.16640598e+00, 5.50440071e+00, 3.30351069e+00,
            1.50971450e+00, 2.11913217e+00, 9.51636875e-01, 5.97982594e+00,
            5.64562943e-01, 6.13533480e+00, 8.65311800e-01, 6.22657169e+00,
            7.59086132e-01, 4.06353680e+00, 2.28776426e+00, 5.86869365e+00,
            1.71816337e+00, 7.85319792e-01, 1.50460617e-01, 2.82091706e+00,
            3.45834634e+00, 2.06116650e+00, 4.58527693e+00, 5.79947743e+00,
            2.64811641e-02, 6.96668845e-03, 1.72518524e+00, 9.13409878e-02,
            4.69873264e-01, 2.22408347e+00, 1.35055799e+00, 6.26325908e+00,
            3.50543804e+00, 1.42601894e+00, 2.54148995e+00, 1.51263372e+00,
            4.96004538e+00, 1.49959722e+00, 1.59323518e+00, 7.95834174e-01,
            5.19614140e+00, 2.47412341e+00, 6.20467413e+00, 1.67757866e+00,
            1.10487798e+00, 4.41227976e+00, 5.32210320e+00, 4.80803524e+00,
            9.88892097e-01, 5.98463492e+00, 1.19588794e+00, 3.98557115e-01,
            1.72771985e+00, 8.22784372e-01, 2.69500149e+00, 7.64328427e-02,
            1.15340893e-01, 5.54926449e+00, 1.12720509e+00, 5.61999098e+00,
            1.98677006e+00, 1.42942748e-01, 2.12902634e+00, 5.18452904e-01,
            1.11413470e+00, 5.18467429e-01, 9.43819250e-01, 1.60335333e+00,
            5.70264704e+00, 1.63637919e+00, 4.54878581e+00, 1.28648700e+00,
            8.39716383e-01, 7.61716895e-01, 2.02483505e+00, 1.19147693e+00,
            2.39297313e+00, 8.05750918e-01, 1.34693205e+00, 6.14495794e-01,
            7.51342927e-01, 1.65406822e-01, 1.10443250e+00, 1.56776394e+00,
            1.01544727e+00, 5.37987280e+00, 1.42073483e+00, 2.60751286e-01,
            2.81388387e+00, 1.94028580e+00, 5.65047260e+00, 6.08005537e+00,
            2.52772277e+00, 4.58822630e+00, 9.40407100e-01, 1.51595542e+00,
            4.83822582e+00, 9.14689597e-01, 7.89979596e-01, 1.09945072e+00,
            8.43851211e-01, 3.25816713e+00, 3.46107407e+00, 2.50285816e+00,
            2.66580004e+00, 4.07139191e+00, 1.92824308e+00, 1.30082616e+00,
            5.31704227e+00, 9.03706705e-01, 1.41551638e+00, 1.18309314e+00,
            3.85822523e+00, 2.26469053e-01, 1.53381650e+00, 6.11428203e+00,
            6.20787549e+00, 7.75303269e-01, 4.73407596e-02, 5.73404907e+00,
            1.53755213e+00, 4.36635351e-01, 1.22269421e+00, 6.24133775e+00,
            4.77486725e+00, 1.55740758e+00, 1.04346206e+00, 2.46201495e+00,
            9.38969009e-01, 2.95780074e+00, 1.55750288e+00, 4.18964784e+00,
            1.49773230e+00, 1.21420593e+00, 1.06905021e+00, 5.72152359e-01,
            4.58683384e+00, 6.04873889e+00, 5.98976085e-01, 1.85594653e+00,
            1.49335177e+00, 1.17051701e+00, 4.27066970e+00, 4.38307268e+00,
            1.29518879e+00, 6.21477235e-01, 2.31764888e+00, 1.81546950e+00,
            2.59389766e+00, 5.29361842e+00, 2.14056486e+00, 5.95763378e+00,
            1.14751266e+00, 4.98931093e+00, 5.15904433e+00, 5.91155150e+00,
            2.02918766e-01, 4.92394579e+00, 6.17530557e+00, 2.58673742e+00,
            9.70702137e-02, 1.40923410e+00, 1.61671780e+00, 1.45245569e+00,
            1.77989899e+00, 2.52877131e+00, 2.70767154e+00, 7.79778701e-01,
            1.00413227e+00, 1.23766338e+00, 4.56845540e-01, 3.85299530e+00,
            6.20287634e+00, 1.81670941e-01, 3.00327854e-01, 5.87190882e+00,
            8.37544131e-01, 5.33789762e+00, 7.93137113e-01, 2.36687516e+00,
            9.82386345e-01, 2.28935626e+00, 1.49384190e+00, 6.48684770e-01,
            1.67428596e+00, 4.91356293e-01, 1.51129716e+00, 1.71459792e+00,
            3.39815782e+00, 1.30041073e+00, 4.41626739e-01, 3.67906830e+00,
            5.13509425e+00, 3.97345386e+00, 4.01693009e-01, 2.22299286e+00,
            1.12493458e+00, 9.71828394e-01, 3.75692408e+00, 7.83255664e-01,
            2.53830319e+00, 5.72882844e+00, 3.90150997e+00, 5.19392797e-01,
            5.31036647e+00, 3.70945512e-01, 1.24232541e+00, 1.54054286e+00,
            1.19543312e+00, 6.26817313e+00, 7.86197031e-01, 3.23304334e+00,
            5.61042471e+00, 2.81179622e+00, 8.34258335e-01, 1.79179798e+00,
            6.02940106e+00, 1.97352187e+00, 6.25222038e+00, 2.59850920e+00,
            5.63029535e-01, 1.89206076e+00, 4.98544872e+00, 2.64987859e+00,
            5.83105384e+00, 1.15545952e+00, 3.62180453e-01, 5.99280627e+00,
            6.24695917e+00, 7.90834082e-01, 4.73312287e-01, 2.52009129e+00,
            5.78700862e+00, 1.64202135e+00, 1.32158703e+00, 1.91444436e+00,
            4.11308463e+00, 8.12012993e-01, 1.80496937e+00, 1.70195740e+00,
            5.30298428e-01, 2.61808988e+00, 5.93601345e-01, 5.44982345e-02,
            1.57660466e+00, 2.64244825e+00, 4.92712752e-01, 7.50699936e-01,
            3.33713720e+00, 1.20011435e+00, 1.10070221e+00, 7.50544899e-01,
            6.50890101e-01, 4.17647519e-01, 1.84698034e+00, 2.28457510e+00,
            4.38688269e-01, 4.82778672e+00, 5.09037850e-01, 2.04589664e+00,
            1.26325867e+00, 5.96889844e+00, 2.57104528e+00, 2.05349986e+00,
            1.89919686e+00, 5.38767440e+00, 1.82975019e+00, 4.08873606e-01,
            4.69807088e+00, 2.02884510e+00, 6.75175866e-01, 1.51212563e+00,
            5.86155891e+00, 6.01368947e+00, 9.17133155e-01, 3.04173735e+00,
            2.57226233e+00, 1.08704944e+00, 1.58251833e+00, 9.43210643e-01,
            5.05053693e-01, 1.90737584e+00, 1.77795587e+00, 5.37004374e+00]),
     [<matplotlib.lines.Line2D at 0x273f6ba69e8>])




![png](output_13_1.png)


## q_vonmises()

- <b>Parameters:</b>
    - p: float/int or list, vector containing the probabilities at which the quantiles are to be calculated
    - mu: float/int, location parameter
    - kappa: float/int, scale parameter. Large values of kappa corresponds to lower variance
- <b>Returns:</b>
    - value: list, quantiles for the given probabilities for a von Mises distribution


```python
circular_stat.q_vonmises(0.5,1,6)
```




    array([1.])



## d_vonmises()

- <b>Parameters:</b>
    - q: float/int or list, vector containing the points at which the CDF is to be calculated
    - mu: float/int, location parameter
    - kappa: float/int, scale parameter. Large values of kappa corresponds to lower variance
- <b>Returns:</b>
    - result: list, Cumulative Distribution Function (CDF) value at the given points for a von Mises distribution


```python
circular_stat.d_vonmises(1,1,6)
```




    array([0.95498257])



### p_vonmises()

- <b>Parameters:</b>
    - q: float/int or list, vector containing the points at which the CDF is to be calculated
    - mu: float/int, location parameter
    - kappa: float/int, scale parameter. Large values of kappa corresponds to lower variance
- <b>Returns:</b>
    - result: list, Cumulative Distribution Function (CDF) value at the given points for a von Mises distribution


```python
circular_stat.p_vonmises([2,0.8],2,6)
```




    array([0.5       , 0.00359546])



### angles_VMF_mix()

- <b>Parameters:</b>
    - x: float/int or list, vector containing the points at which the density is to be calculated
    - mu: float/int, location parameter
    - kappa: float/int, scale parameter. Large values of kappa corresponds to lower variance
- <b>Returns:</b>
    - pdf: list, Probability Distribution Function (PDF) value at the given points for a von Mises distribution


```python
## Sample simulated data for demo purposes for 'angles_VMF_mix'
ls = [10,15,20,25,100,110,120,130,140]
```


```python
circular_stat.angles_VMF_mix(ls,2)
```




    ([2.094395100371017, 0.3054326188103176],
     [17.272339492503747, 105.9312216142795],
     [0.5555555566516756, 0.4444444433483244])



### vmf_clust()

- <b>Parameters:</b>
    - main_df: Data file with rows and features in a dataframe format
    - num_clusters: Number of clusters 
- <b>Returns:</b>
    - mu: list of the mixtures, location parameter
    - kappa: list of the mixtures, scale parameter. Large values of kappa corresponds to lower variance 
    - p_i: mixture proportions of each mixture/cluster summing to 1
    - final_df: final data table output with the cluster confidence % and a hard cluster assigned based on maximum PDF


```python
## Simulated data (or any dataset can be loaded in to the variable 'main_df' from outside)
## Sample simulated data for demo purposes for 'vmf_clust'
import numpy as np
import pandas as pd
c = [[x,y] for x,y in zip(list(np.random.normal(100,20,500)) , list(np.random.normal(50,10,500)))]
d = [[x,y] for x,y in zip(list(np.random.normal(50,10,1000)) , list(np.random.normal(0,10,1000)))]
e = [[x,y] for x,y in zip(list(np.random.normal(50,10,750)) , list(np.random.normal(100,20,750)))]
dat_raw = c+d+e
main_df = pd.DataFrame(dat_raw,columns=['feature-1','feature-2'])
```


```python
circular_stat.vmf_clust(main_df,3)
```

    mean 0 is: [0.892131032374116, 0.451776738085411]
    kappa 0 is: 70.00834916361028
    proportion 0 is: 0.231167905183219
    mean 1 is: [0.9999896452358933, -0.00455076048506396]
    kappa 1 is: 27.343100441832927
    proportion 1 is: 0.437525969173756
    mean 2 is: [0.4491917901329271, 0.8934353561826263]
    kappa 2 is: 78.61673014888608
    proportion 2 is: 0.3313061256430249
    




    ([array([0.89213103, 0.45177674]),
      array([ 0.99998965, -0.00455076]),
      array([0.44919179, 0.89343536])],
     [70.00834916361028, 27.343100441832927, 78.61673014888608],
     [0.231167905183219, 0.437525969173756, 0.3313061256430249],
            feature-1   feature-2     cluster-0     cluster-1  cluster-2  \
     0     139.471351   45.882628  1.503302e+00  8.936243e-02   0.001775   
     1     119.938467   51.715813  2.916955e+00  9.464533e-03   0.023160   
     2     121.616333   57.387580  3.242680e+00  3.536805e-03   0.053548   
     3     100.569302   48.349254  3.282760e+00  2.837595e-03   0.063457   
     4      89.260758   41.219180  3.183056e+00  4.532329e-03   0.043905   
     5      61.719914   41.400288  1.978768e+00  1.912480e-05   0.880617   
     6      87.185001   60.382212  1.729603e+00  1.058840e-05   1.069765   
     7      93.051261   46.899498  3.331571e+00  1.580926e-03   0.096873   
     8     121.215026   39.089465  1.411511e+00  1.016981e-01   0.001473   
     9      85.965893   53.971909  2.480114e+00  6.103953e-05   0.566188   
     10    129.615250   40.986347  1.324970e+00  1.150098e-01   0.001227   
     11     91.256978   19.902307  3.523517e-01  6.180382e-01   0.000049   
     12     93.958635   59.604592  2.404868e+00  5.117872e-05   0.608749   
     13     84.811891   48.922673  3.003518e+00  2.384069e-04   0.300546   
     14    126.075665   51.839666  2.683585e+00  1.510252e-02   0.014774   
     15    115.934662   47.819874  2.699846e+00  1.465836e-02   0.015221   
     16    121.484124   50.128095  2.701824e+00  1.460489e-02   0.015277   
     17     85.910685   72.723926  4.967720e-01  1.675352e-07   2.608255   
     18    110.474384   62.684016  3.080500e+00  3.058700e-04   0.263653   
     19     99.560280   49.340523  3.323283e+00  1.956895e-03   0.083397   
     20     74.999141   47.347572  2.440215e+00  5.558118e-05   0.588580   
     21     74.112295   63.858375  4.299277e-01  1.122662e-07   2.737970   
     22    121.159789   54.387732  3.085891e+00  6.199454e-03   0.033768   
     23     63.220178   35.054237  3.171805e+00  4.296815e-04   0.218703   
     24    122.727437   56.981211  3.199246e+00  4.262457e-03   0.046151   
     25     88.099036   43.124422  3.310665e+00  2.280528e-03   0.074665   
     26    117.115791   36.184567  1.227607e+00  1.323229e-01   0.000990   
     27    106.116573   49.800459  3.228876e+00  3.768706e-03   0.050932   
     28    113.811790   50.836143  3.066846e+00  6.540865e-03   0.032240   
     29     94.932897   50.369766  3.289901e+00  8.004002e-04   0.151301   
     ...          ...         ...           ...           ...        ...   
     2220   62.309846  124.814158  3.337542e-06  3.628784e-17   0.091936   
     2221   56.841912  131.711926  3.005120e-07  1.054942e-18   0.024249   
     2222   44.583509  113.497529  6.616372e-08  1.231152e-19   0.009962   
     2223   47.301552  132.172114  1.551619e-08  1.648298e-20   0.004111   
     2224   39.819513   98.140967  1.108230e-07  2.544943e-19   0.013546   
     2225   46.612276   80.932605  3.620726e-05  1.439147e-15   0.304873   
     2226   41.249140  103.992841  7.720880e-08  1.529076e-19   0.010926   
     2227   58.833949   60.070073  8.151169e-02  1.913281e-09   3.321114   
     2228   50.519667  101.399315  3.228160e-06  3.451465e-17   0.090326   
     2229   33.920179  123.613736  3.487457e-10  1.033828e-22   0.000356   
     2230   33.940512   99.177198  7.888406e-09  6.547220e-21   0.002693   
     2231   59.581237  112.461518  9.006889e-06  1.640543e-16   0.153947   
     2232   54.955239  106.202924  6.075780e-06  8.984563e-17   0.125813   
     2233   37.045666   47.784020  3.922029e-03  4.212383e-12   1.926507   
     2234   49.607915   94.661874  7.508516e-06  1.241231e-16   0.140298   
     2235   45.148476  132.550782  7.352049e-09  5.950335e-21   0.002576   
     2236   57.733814   88.722173  2.664508e-04  3.725767e-14   0.739151   
     2237   49.860347  122.752343  1.128026e-07  2.609454e-19   0.013688   
     2238   36.639207   78.868609  1.008746e-06  6.129664e-18   0.048057   
     2239   48.712224  120.532894  1.040402e-07  2.327676e-19   0.013048   
     2240   47.645999   92.155213  5.990806e-06  8.793930e-17   0.124899   
     2241   52.889724  143.961495  2.321336e-08  2.868774e-20   0.005272   
     2242   50.746901  116.786158  3.360447e-07  1.238988e-18   0.025857   
     2243   48.925500   88.414243  1.862585e-05  5.054305e-16   0.221296   
     2244   51.115721  124.711098  1.304037e-07  3.204067e-19   0.014911   
     2245   49.656761   94.137786  8.374910e-06  1.467224e-16   0.148351   
     2246   52.005024  115.979223  5.624189e-07  2.610222e-18   0.034663   
     2247   61.875808   92.146614  4.396858e-04  8.689050e-14   0.904196   
     2248   52.746164  138.201844  4.201264e-08  6.527615e-20   0.007575   
     2249   30.474602  107.309992  5.519577e-10  1.884192e-22   0.000483   
     
             cluster   max-pdf  total_pdf  %confidence  
     0     cluster-0  1.503302   1.594439    94.284042  
     1     cluster-0  2.916955   2.949579    98.893935  
     2     cluster-0  3.242680   3.299764    98.270041  
     3     cluster-0  3.282760   3.349055    98.020507  
     4     cluster-0  3.183056   3.231493    98.501074  
     5     cluster-0  1.978768   2.859404    69.202116  
     6     cluster-0  1.729603   2.799378    61.785235  
     7     cluster-0  3.331571   3.430025    97.129653  
     8     cluster-0  1.411511   1.514682    93.188605  
     9     cluster-0  2.480114   3.046363    81.412298  
     10    cluster-0  1.324970   1.441207    91.934766  
     11    cluster-1  0.618038   0.970439    63.686443  
     12    cluster-0  2.404868   3.013668    79.798707  
     13    cluster-0  3.003518   3.304302    90.897196  
     14    cluster-0  2.683585   2.713461    98.898955  
     15    cluster-0  2.699846   2.729725    98.905399  
     16    cluster-0  2.701824   2.731706    98.906117  
     17    cluster-2  2.608255   3.105027    84.001038  
     18    cluster-0  3.080500   3.344459    92.107585  
     19    cluster-0  3.323283   3.408636    97.495959  
     20    cluster-0  2.440215   3.028850    80.565718  
     21    cluster-2  2.737970   3.167898    86.428607  
     22    cluster-0  3.085891   3.125858    98.721398  
     23    cluster-0  3.171805   3.390938    93.537691  
     24    cluster-0  3.199246   3.249659    98.448641  
     25    cluster-0  3.310665   3.387611    97.728615  
     26    cluster-0  1.227607   1.360919    90.204228  
     27    cluster-0  3.228876   3.283577    98.334110  
     28    cluster-0  3.066846   3.105627    98.751281  
     29    cluster-0  3.289901   3.442002    95.581027  
     ...         ...       ...        ...          ...  
     2220  cluster-2  0.091936   0.091940    99.996370  
     2221  cluster-2  0.024249   0.024249    99.998761  
     2222  cluster-2  0.009962   0.009962    99.999336  
     2223  cluster-2  0.004111   0.004111    99.999623  
     2224  cluster-2  0.013546   0.013546    99.999182  
     2225  cluster-2  0.304873   0.304910    99.988125  
     2226  cluster-2  0.010926   0.010926    99.999293  
     2227  cluster-2  3.321114   3.402626    97.604448  
     2228  cluster-2  0.090326   0.090329    99.996426  
     2229  cluster-2  0.000356   0.000356    99.999902  
     2230  cluster-2  0.002693   0.002693    99.999707  
     2231  cluster-2  0.153947   0.153956    99.994150  
     2232  cluster-2  0.125813   0.125819    99.995171  
     2233  cluster-2  1.926507   1.930429    99.796831  
     2234  cluster-2  0.140298   0.140306    99.994648  
     2235  cluster-2  0.002576   0.002576    99.999715  
     2236  cluster-2  0.739151   0.739417    99.963965  
     2237  cluster-2  0.013688   0.013688    99.999176  
     2238  cluster-2  0.048057   0.048058    99.997901  
     2239  cluster-2  0.013048   0.013048    99.999203  
     2240  cluster-2  0.124899   0.124905    99.995204  
     2241  cluster-2  0.005272   0.005272    99.999560  
     2242  cluster-2  0.025857   0.025857    99.998700  
     2243  cluster-2  0.221296   0.221315    99.991584  
     2244  cluster-2  0.014911   0.014912    99.999125  
     2245  cluster-2  0.148351   0.148359    99.994355  
     2246  cluster-2  0.034663   0.034663    99.998377  
     2247  cluster-2  0.904196   0.904636    99.951396  
     2248  cluster-2  0.007575   0.007575    99.999445  
     2249  cluster-2  0.000483   0.000483    99.999886  
     
     [2250 rows x 9 columns])

