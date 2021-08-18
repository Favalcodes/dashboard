<script>
import { Line } from "vue-chartjs";

export default {
  extends: Line,
  data () {
        return {
          gradient: null
        }
  },
  mounted() {
      this.gradient = this.$refs.canvas.getContext('2d').createLinearGradient(0, 0, 0, 450)
        this.gradient2 = this.$refs.canvas.getContext('2d').createLinearGradient(0, 0, 0, 450)
    
        this.gradient.addColorStop(0, 'rgba(82, 133, 242, 1)')
        this.gradient.addColorStop(0.5, 'rgba(82, 133, 242, 0)');
        this.gradient.addColorStop(1, 'rgba(82, 133, 242, 0)');

    this.renderChart({
      labels: [
        "Mon",
        "Tue",
        "Wed",
        "Thu",
        "Fri",
        "Sat",
        "Sun"
      ],
      datasets: [
        {
          label: "",
          color: "#647AA8",
          backgroundColor: this.gradient,
          data: [90, 190, 105, 210, 220, 360, 320]
        }
      ]
    },
    {
    legend: {
      display: false
    },
    scales: {
        yAxes: [{
        ticks: {
            min: 0,
            max: 400,
            stepSize: 100,
          beginAtZero: true
        },
        gridLines: {
          color: "#647AA809",
        }
      }],
      xAxes: [{
        gridLines: {
          display: false
        }
      }]
    },
    elements: { 
      point: {
        radius: 0
      }
    },
    responsive: true,
    maintainAspectRatio: false
  });
  },
};
</script>