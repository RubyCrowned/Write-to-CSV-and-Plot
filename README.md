# Write-to-CSV-and-Plot
 with open("test_data.csv","a") as f:
            writer = csv.writer(f,delimiter=",")
            writer.writerow([time.time(),decoded_bytes])
        y_var = np.append(y_var,decoded_bytes)
        y_var = y_var[1:plot_window+1]
        line.set_ydata(y_var)
        ax.relim()
        ax.autoscale_view()
        fig.canvas.draw()
        fig.canvas.flush_events()
        time.sleep(.5)
