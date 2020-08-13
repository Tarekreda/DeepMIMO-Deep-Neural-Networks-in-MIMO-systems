# DeepMIMO-Deep-Neural-Networks-in-MIMO-systems
In recent years, the world is witnessing a revolution in deep machine
learning. In many fields of engineering, e.g., computer vision, it was shown
that computers can be fed with sample pairs of inputsand desired outputs,
and “learn” the functions which relates them. These rules can then be used
to classify (detect) the unknown outputs of future inputs. We will apply
deep machine learning in the classical MIMO detection problem and
understand its advantages and disadvantages.
The binary MIMO detection setting is a classical problemin simple
hypothesis testing . The maximum likelihood(ML) detector is the optimal
detector in the sense of minimum joint probability of error for detecting all
the symbols simultaneously. It can be implemented via efficient search
algorithms, e.g., the sphere decoder . The difficulty is that its worst case
computational complexity is impractical for many applications.
Consequently, several modified search algorithms have been purposed,
offering improved complexity performance.
In the context of MIMO detection, a model is known and allows us to
generate as many synthetic examples as needed. Therefore we adapt an
alternative notion. We interpret “learning” as the idea of choosing a best
decoder from a prescribed class of algorithms. Classical detection theory
tries to choose the best estimate of the unknowns, whereas machine
learning tries to choose the best algorithm to be applied.
In recent years, deep learning methods have been purposed for improving
the performance of a decoder for linear codes in fixed channels. And in
several applications of deeplearning for communication applications have
been considered, including decoding signals over fading channels, but the
architecture purposed there does not seem to be scalable for higher
dimension signals.
<br />
- Coding steps:
<br />we formulate the MIMO detection problem in a machine learning
framework. We consider the standard linear MIMO model:

                      y = Hx + w (1)

We assume perfect channel state information (CSI) and that the channel H
is exactly known. However, we differentiatebetween two possible cases:
Fixed Channel (FC): In the FC scenario, H is deterministic and constant (or a realization of a degenerate distribution which only takes a single value).
Varying Channel (VC): In the VC scenario, we assume H random with a
known distribution. Our goal is to detect x, using an algorithm that receives
y and H as inputs and estimates ^x.
To find the best detector, we fix a loss function (x; ^x (H; y)) that
measures the distance between the true symbols and their estimates. Then,
we find  by minimizing the loss function we chose over the MIMO model
distribution:

                  min{Efl (x; ^x(H; y))g } (2)

 - method 1 : The goal in detection is to decrease the probability of
error. Therefore, the best loss function in this problem is choosing an
unrealistically flexible architecture with unbounded
parameterization and no restrictions such that
