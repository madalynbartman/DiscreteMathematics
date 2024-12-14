## Classes of Functions
### Injective Function
f: X ⇒ Y, a, b ∈ X, if a ≠ b, then f(a) ≠ f(b)
![](https://github.com/jongwoojeff/DiscreteMathematics/blob/master/images/injective.png)
maps distinct elements of its domain to distinct elements of its codomain

### Surjective Function
f: X ⇒ Y, for all b ∈ Y, there exits at least one a ∈ X such that f(a) = b
![](https://github.com/jongwoojeff/DiscreteMathematics/blob/master/images/surjective.png)
the function f may map one or more elements of X to the same element of Y

### Bijective Function
Injective as well as surjective
![](https://github.com/jongwoojeff/DiscreteMathematics/blob/master/images/bijective.png)
each element of the codomain is mapped to by exactly one element of the domain

### Examples:
Determine the class

**1. f: Z ⇒ R, f(x) = (3 - x)/2**

if a ≠ b, f(a) ≠ f(b). Therefore, Injective.

**2. C = {c|c >= 0, c is a real number}, f: R ⇒ C, f(x): |x|**

Every element in C has at least one corresponding input. Therefore, Surjective.

**3. f: Z ⇒ Z, f(x) = x + 1**

both injective and surjective; therefore, Bijective
## Function Composition 
when f: A ⇒ B and g: B ⇒ C, function composition can be expressed as g(f(x)) or g ∘ f
![](https://github.com/jongwoojeff/DiscreteMathematics/blob/master/images/func-comp.png)

## Useful tips for Function Composition
when f: A ⇒ B and g: B ⇒ C and g ∘ f is a function composition

1. if both f and g are injective, g ∘ f is injective

2. if both f and g are surjective, g ∘ f is surjective

3. if both f and g are bijective, g ∘ f is bijective

4. if g ∘ f is injective, f is injective

5. if g ∘ f surjective, g is surjective

6. if g ∘ f is bijective, f is injective and g is surjective