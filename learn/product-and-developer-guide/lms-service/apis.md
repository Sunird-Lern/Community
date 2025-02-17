# APIs

#### API Documentation:

Refer to \*\*\*\* the below various API documentation related to all the different APIs that are being consumed with in all the batch jobs.

#### Course Batch Management APIs are listed below:

{% swagger src="../../../.gitbook/assets/coursebatchmanapi (1) (2).yaml" path="/course/v1/batch/read/{batch-id}" method="get" %}
[coursebatchmanapi (1) (2).yaml](<../../../.gitbook/assets/coursebatchmanapi (1) (2).yaml>)
{% endswagger %}

{% swagger src="../../../.gitbook/assets/coursebatchmanapi (1) (1) (2).yaml" path="/course/v1/batch/update" method="patch" expanded="true" fullWidth="false" %}
[coursebatchmanapi (1) (1) (2).yaml](<../../../.gitbook/assets/coursebatchmanapi (1) (1) (2).yaml>)
{% endswagger %}

{% swagger src="../../../.gitbook/assets/coursebatchmanapi (1) (2).yaml" path="/course/v1/batch/list" method="post" %}
[coursebatchmanapi (1) (2).yaml](<../../../.gitbook/assets/coursebatchmanapi (1) (2).yaml>)
{% endswagger %}

{% swagger src="../../../.gitbook/assets/coursebatchmanapi (1) (1) (4).yaml" path="/course/v1/batch/create" method="post" %}
[coursebatchmanapi (1) (1) (4).yaml](<../../../.gitbook/assets/coursebatchmanapi (1) (1) (4).yaml>)
{% endswagger %}

#### Course Enrolment APIs are listed below:

{% swagger src="../../../.gitbook/assets/courseenrolmentapi (1) (1) (2).yaml" path="/course/v1/enrol" method="post" %}
[courseenrolmentapi (1) (1) (2).yaml](<../../../.gitbook/assets/courseenrolmentapi (1) (1) (2).yaml>)
{% endswagger %}

{% swagger src="../../../.gitbook/assets/courseenrolmentapi (1) (1) (2).yaml" path="/course/v1/unenrol" method="post" %}
[courseenrolmentapi (1) (1) (2).yaml](<../../../.gitbook/assets/courseenrolmentapi (1) (1) (2).yaml>)
{% endswagger %}

{% swagger src="../../../.gitbook/assets/courseenrolmentapi (1) (1) (1).yaml" path="/course/v1/user/enrollment/list/{user-id}" method="get" %}
[courseenrolmentapi (1) (1) (1).yaml](<../../../.gitbook/assets/courseenrolmentapi (1) (1) (1).yaml>)
{% endswagger %}

#### Course Progress APIs are listed below:

{% swagger src="../../../.gitbook/assets/courseprogressapi (1) (1).yaml" path="/course/v1/content/state/read" method="post" %}
[courseprogressapi (1) (1).yaml](<../../../.gitbook/assets/courseprogressapi (1) (1).yaml>)
{% endswagger %}

{% swagger src="../../../.gitbook/assets/courseprogressapi (1) (1).yaml" path="/course/v1/content/state/update" method="patch" %}
[courseprogressapi (1) (1).yaml](<../../../.gitbook/assets/courseprogressapi (1) (1).yaml>)
{% endswagger %}

#### Course Batch Certificates APIs are listed below:

{% swagger src="../../../.gitbook/assets/coursebatchcertificateapi (1).yaml" path="/course/batch/cert/v1/template/add" method="patch" %}
[coursebatchcertificateapi (1).yaml](<../../../.gitbook/assets/coursebatchcertificateapi (1).yaml>)
{% endswagger %}

{% swagger src="../../../.gitbook/assets/coursebatchcertificateapi.yaml" path="/course/batch/cert/v1/template/remove" method="patch" %}
[coursebatchcertificateapi.yaml](../../../.gitbook/assets/coursebatchcertificateapi.yaml)
{% endswagger %}

#### Group Activity Aggregator

{% swagger src="../../../.gitbook/assets/groupactivityapi.yaml" path="/data/v1/group/activity/agg" method="post" %}
[groupactivityapi.yaml](../../../.gitbook/assets/groupactivityapi.yaml)
{% endswagger %}

#### Collection Summary

## Collection Summary(https://staging.open-sunbird.org/report/v1/collection/summary)

<mark style="color:green;">`POST`</mark>&#x20;

This API gives the collection summary, like the total number of enrolments, completion count, count of certificates issued.

#### Request Body

| Name                                           | Type         | Description                                                                                                             |
| ---------------------------------------------- | ------------ | ----------------------------------------------------------------------------------------------------------------------- |
| request<mark style="color:red;">\*</mark>      | Object       |                                                                                                                         |
| filters<mark style="color:red;">\*</mark>      | Object       | Search filters                                                                                                          |
| collectionId<mark style="color:red;">\*</mark> | String       | Id of the collection                                                                                                    |
| batchId<mark style="color:red;">\*</mark>      | String       | Id of the batch                                                                                                         |
| group\_by                                      | String Array | `"state", "dist"`                                                                                                       |
| intervals                                      | String       | `2019-09-23T00:00:00.000Z/2019-09-24T00:00:00.000Z"` St`artDate - Batch Start Date and  Default EndDate - Current Date` |

{% tabs %}
{% tab title="200: OK " %}
```javascript
{
  "result": {
    "collectionId": "", // Collection/CourseId
    "name": "", // Collection Name
    "batchId": "", // Batch Identifier
    "enrolmentCount": "",
    "completionCount": "",
    "certificatesIssuedCount": "",
    "summary": {  // Summary by state and district level
      "state": {
        "enrolmentCount": "",
        "completionCount": ""
      },
      "district": {
        "enrolmentCount": "",
        "completionCount": ""
      }
    }
  }
}
```
{% endtab %}
{% endtabs %}

#### Page APIs

{% swagger src="../../../.gitbook/assets/pagesapi.yaml" path="/data/v1/page/create" method="post" %}
[pagesapi.yaml](../../../.gitbook/assets/pagesapi.yaml)
{% endswagger %}

{% swagger src="../../../.gitbook/assets/pagesapi.yaml" path="/data/v1/page/update" method="patch" %}
[pagesapi.yaml](../../../.gitbook/assets/pagesapi.yaml)
{% endswagger %}

{% swagger src="../../../.gitbook/assets/pagesapi.yaml" path="/data/v1/page/read/{pageName}" method="get" %}
[pagesapi.yaml](../../../.gitbook/assets/pagesapi.yaml)
{% endswagger %}

{% swagger src="../../../.gitbook/assets/pagesapi.yaml" path="/data/v1/page/section/create" method="post" %}
[pagesapi.yaml](../../../.gitbook/assets/pagesapi.yaml)
{% endswagger %}

{% swagger src="../../../.gitbook/assets/pagesapi.yaml" path="/data/v1/page/section/update" method="patch" %}
[pagesapi.yaml](../../../.gitbook/assets/pagesapi.yaml)
{% endswagger %}

{% swagger src="../../../.gitbook/assets/pagesapi.yaml" path="/data/v1/page/section/read/{SectionId}" method="get" %}
[pagesapi.yaml](../../../.gitbook/assets/pagesapi.yaml)
{% endswagger %}

{% swagger src="../../../.gitbook/assets/pagesapi.yaml" path="/data/v1/page/section/list" method="get" %}
[pagesapi.yaml](../../../.gitbook/assets/pagesapi.yaml)
{% endswagger %}

{% swagger src="../../../.gitbook/assets/proxy-result.yml" path="/api/course/v1/jobrequest/submit" method="post" %}
[proxy-result.yml](../../../.gitbook/assets/proxy-result.yml)
{% endswagger %}

{% swagger src="../../../.gitbook/assets/proxy-result.yml" path="/api/course/v1/jobrequest/list/{tag}" method="get" %}
[proxy-result.yml](../../../.gitbook/assets/proxy-result.yml)
{% endswagger %}
