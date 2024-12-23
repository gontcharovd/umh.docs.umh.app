---
title: 3. Data Visualization
menuTitle: 3. Data Visualization
description: Build a simple Grafana dashboard with the gathered data.
weight: 4000
---

After bringing the data from the OPC UA simulator into your Unified Namespace,
you can use **Grafana** to create dashboards to display it. If you haven't
already connected the OPC UA simulator to your instance, you can follow the
[previous guide](https://umh.docs.umh.app/docs/getstarted/dataacquisitionmanipulation/).

## Accessing Grafana

1. Make sure you are on the same network as your instance to access Grafana.

2. In the Management Console, select **Applications** from the left hand
menu. Click on **Historian (Grafana)** for the instance to which you have
connected the OPC UA simulator. You can search for your instance's applications
by entering its name in the **Filter by name or instance** field at the top of
the page.

3. Click on the URL displayed in the side panel that opens. This will only work
if you have set the correct IP address for your instance during the
installation script. If you can't connect to Grafana, find out the IP address
of your instance and enter the following URL in your browser

    ```markdown
    http://<IP-address-of-your-instance>:8080
    ```

4. Copy the Grafana password by clicking on it in the side panel of the
application. The user name is `admin`.

5. To add a dashboard, click on **Dashboards** in the left menu and then on the
blue **+ Create Dashboard** button in the middle of the page. On the next page
click **+ Add visualisation**.

6. Select the **UMH TimescaleDB** data source in the **Select data source**
dialogue box.

7. To access data from your Unified Namespace in Grafana, you can use SQL
queries generated by the Management Console for each tag. Open the
**Tag Browser** and navigate to the desired tag, e.g. **CurrentTemperature**
from the **ParameterSet** folder of the OPC UA Simulator. The query is located
at the bottom of the page under **SQL Query**. Make sure it is set to
**Grafana** and then copy it.

8. In Grafana, change the query mode to **Code** by toggling the
**Builder/Code** switch located on the right hand side of the page next to the
blue **Run query** button. Paste the query you copied from the Management
Console into the text box.

9. Click the blue **Run query** button. If everything is set up correctly you
should see the data displayed in a graph.

10. There are many ways to customise the graph on the right hand side of the
page. For example, you can use different colours or chart styles. You can also
add more queries at the bottom of the page.

11. When you are happy, click the blue **Apply** button in the top right
corner. You will now see the dashboard. You can adjust the size and position
of the graph or access other options by clicking on the three dots in the top
right hand corner of the graph. To add another graph, click **Add** and then
**Visualisation** from the menu bar at the top of the page.

12. To save your dashboard, press `Ctrl` + `S`.

## Further Reading

If you would like to find out more about the United Manufacturing Hub, here
are some links to get you links to get you started.

**General knowledge, updates and guidance? Check out our Learn page:**

- [Our Blog](https://learn.umh.app/)
- [Grafana Guides](https://learn.umh.app/topic/best-practices-and-guides-for-grafana/)

**Do you need more technical background information?**

- [Introduction IT](https://learn.umh.app/course/introduction-into-it-ot-information-technology/)
- [Introduction OT](https://learn.umh.app/course/introduction-into-it-ot-operational-technology-ot/)
- [Introduction IIoT](https://learn.umh.app/course/introduction-into-it-ot-industrial-internet-of-things-iiot/)
- [The Architecture of the UMH](https://umh.docs.umh.app/docs/architecture/)

**If you don't want to read all that, you can check out our**
**[YouTube channel](https://www.youtube.com/@unitedmanufacturinghub)**
**where we have also covered these topics:**

- [Unified Namespace (UNS) Basics](https://www.youtube.com/watch?v=ywiHxnm2Bnk&list=PLeC0OzgWYQfuD9Jb2eUoSbv5Vu0xxSm0k)
- [Introduction into IT / OT](https://www.youtube.com/watch?v=EuHP8olZQ8I&list=PLeC0OzgWYQfshVdn_-XCEXB4zh54ekW0b)

**If you need help, want to stay up to date with product news, or just want**
**to connect with like-minded people, join our community:**

- [Discord](https://community-discord.umh.app/?ref=learn.umh.app)
- [Linked In](https://www.linkedin.com/company/united-manufacturing-hub?ref=learn.umh.app)
- [GitHub](https://github.com/united-manufacturing-hub/united-manufacturing-hub?ref=learn.umh.app)
