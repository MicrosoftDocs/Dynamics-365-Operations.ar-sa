---
title: إعداد مراحل أمر الخدمة
description: إعداد مراحل أمر الخدمة.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b6e245b351b66724eedf8e0d1a0ebf0202df857
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824404"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="0caf6-103">إعداد مراحل أمر الخدمة</span><span class="sxs-lookup"><span data-stu-id="0caf6-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="0caf6-104">انتقل إلى **إدارة الخدمة** \> **الإعداد** \> **أوامر الخدمة** \> **مراحل الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="0caf6-104">Go to **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="0caf6-105">حدد **جديد** لإنشاء سجل جديد.</span><span class="sxs-lookup"><span data-stu-id="0caf6-105">Select **New** to create a new record.</span></span>

3.  <span data-ttu-id="0caf6-106">في حقلي **مرحلة الخدمة** و **الوصف**، حدد معرف مرحلة الخدمة والوصف.</span><span class="sxs-lookup"><span data-stu-id="0caf6-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="0caf6-107">حدد المحددات المناسبة للمرحلة.</span><span class="sxs-lookup"><span data-stu-id="0caf6-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="0caf6-108">حدد المرحلة الأصلية للمرحلة الحالية أو اترك الحقل **الأصل** فارغًا إذا كانت المرحلة الموجودة في المرحلة الأولية في إعداد المرحلة.</span><span class="sxs-lookup"><span data-stu-id="0caf6-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0caf6-109">لا يمكن تعديل حقل <STRONG>الأصل</STRONG> بعد حفظ المرحلة.</span><span class="sxs-lookup"><span data-stu-id="0caf6-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="0caf6-110">بدلاً من ذلك، يمكنك حذف السجل وإنشاؤه مرة أخرى من خلال الاستعانة بتحديد مختلف في حقل <STRONG>الأصل</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="0caf6-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="0caf6-111">أيضًا، يمكن إنشاء مرحلة واحدة مع جعل حقل <STRONG>الأصل</STRONG> فارغًا.</span><span class="sxs-lookup"><span data-stu-id="0caf6-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="0caf6-112">وهذا يعني أنه يتم السماح ببمرحلة أولية واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="0caf6-112">That is, only one initial stage is permitted.</span></span></P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]