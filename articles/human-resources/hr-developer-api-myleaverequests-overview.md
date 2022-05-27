---
title: نظره عامة على MyLeaveRequests
description: يقدم الكيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازة.
author: twheeloc
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20cc53ec3bcf38444ccf75f81e28d5efd9fc4537
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717044"
---
# <a name="myleaverequests-overview"></a>نظره عامة على MyLeaveRequests


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يوفر كيان MyLeaveRequests في Microsoft Dynamics 365 Human Resources قائمة بطلبات الإجازات في النظام، مقيدة (محدودة) على الطلبات التي يمكن الوصول إليها للمستخدم الحالي الذي يقوم بالاستعلام عن الكيان.

## <a name="key"></a>مفتاح

  | اسم الخاصية | نوع البيانات |
  |---------------|-----------|
  | dataAreaId    | سلسلة    |
  | RequestId     | سلسلة    |
  | LeaveType     | سلسلة    |
  | LeaveDate     | التاريخ      |
  
## <a name="properties"></a>خصائص

  | اسم الخاصية     | نوع البيانات | مطلوب |
  |-------------------|-----------|----------|
  | dataAreaId        | سلسلة    | س        |
  | RequestId         | سلسلة    | س        |
  | LeaveType         | سلسلة    | س        |
  | LeaveDate         | التاريخ      | س        |
  | ReasonCodeId      | سلسلة    |          |
  | PersonnelNumber   | سلسلة    | س        |
  | RequestDate       | التاريخ      | س        |
  | تعليق           | سلسلة    |          |
  | الحالة            | تعداد      | س        |
  | ‏‏المقدار            | حقيقي      |          |
  | HalfDayDefinition | تعداد      |          |

## <a name="actions"></a>إجراءات

 | اسم الإجراء                               | ‏‏الوصف                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [إرسال](hr-developer-api-myleaverequests-submit.md)   | أرسل الطلب لمعالجته من خلال سير العمل. |

## <a name="see-also"></a>راجع أيضًا

- [إرسال طلب إجازة إلى سير العمل](hr-developer-api-myleaverequests-submit.md)
- [المصادقة](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
