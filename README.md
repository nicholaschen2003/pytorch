First modification:
c1 = (3, 6, 3)
p1 = (2, 2)
c2 = (6, 16, 3)
p2 = (3, 3, padding = 1)
~62% accuracy


then increased features by x8 in each convolutional layer (linear layers: 4800->2400->800->400->120->84->10)
~72% accuracy

realized it hadn't overfitted yet, so then ran with 50 epochs
~75.39% accuracy

then ran it with a dumb number of features (3->60->920) (linear layers: 23000->10000->4800->2400->800->400->120->84->10)
~77.47% accuracy

then went to a more reasonable x5 multiplier for features (3->15->75->375) and added a third layer
conv3 = (75, 375, 3)
pool3 = (3, 3)
~71-72% accuracy

then used same as last one but increased feature multiplier to 15x
~79% accuracy

then took last one and boosted features as much as i could (5.1/6.0 gb of vram used) (3->100->945->16000) (ll: 16000->8000->4000->1000->400->100->10)
~80.87-80.88% accuracy

went back to x5 multiplier and added batch normalization (15, im not sure if this is right but i think the parameter is the output layers?)
~72.45-74% accuracy
