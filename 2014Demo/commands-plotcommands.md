### plotOutput
<code><pre>
plotOutput(outputId, width = "100%", height = "400px",
    clickId = NULL, hoverId = NULL, hoverDelay = 300,
    hoverDelayType = c("debounce", "throttle"))
</pre></code>

- `outputId` output variable to read the plot from
- `width` Plot width. Must be a valid CSS unit (like "100%", "400px", "auto") or a number, which will be coerced to a string and have "px" appended.
- `height` Plot height
- `clickId` If not NULL, the plot will send coordinates to the server whenever it is clicked. This information will be accessible on the input object using input$clickId. The value will be a named list or vector with x and y elements indicating the mouse position in user units.
- `hoverId` If not NULL, the plot will send coordinates to the server whenever the mouse pauses on the plot for more than the number of milliseconds determined by hoverTimeout. This information will be The value will be NULL if the user is not hovering, and a named list or vector with x and y elements indicating the mouse position in user units.
- `hoverDelay` The delay for hovering, in milliseconds.
- `hoverDelayType` The type of algorithm for limiting the number of hover events. Use "throttle" to limit the number of hover events to one every hoverDelay milliseconds. Use "debounce" to suspend events while the cursor is moving, and wait until the cursor has been at rest for hoverDelay milliseconds before sending an event.

<code><pre>
# Show a plot of the generated distribution
mainPanel(
  plotOutput("distPlot")
)
</pre></code>
<hr>
