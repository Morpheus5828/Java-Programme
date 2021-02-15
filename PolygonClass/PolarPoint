public class PolarPoint {
    private double O;
    private double r;

    public PolarPoint(double O, double r) {
        this.O = O;
        this.r = r;
    }
    public CartesianPoint toCartesian() {
      return new CartesianPoint(this.r*Math.cos(this.O), this.r*Math.sin(this.O));
    }
    public PolarPoint rotate(double alpha) {
        return new PolarPoint(this.O + alpha, this.r);
    }
    @Override
    public String toString() {
        return "PolarPoint{" +
                "θ=" + O +
                ", r=" + r +
                '}';
    }
}
