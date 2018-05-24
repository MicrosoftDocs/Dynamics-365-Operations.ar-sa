---
title: "إعداد مراحل أمر الخدمة"
description: "إعداد مراحل أمر الخدمة."
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6e2556dd8f3f32da16e53bfe46faec7489d84efa
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-service-order-stages"></a><span data-ttu-id="bb749-103">إعداد مراحل أمر الخدمة</span><span class="sxs-lookup"><span data-stu-id="bb749-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="bb749-104">انقر فوق **إدارة الخدمة** \> **الإعداد** \> **أوامر الخدمة** \> **مراحل الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="bb749-104">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="bb749-105">اضغط CTRL+N لإنشاء سجل جديد.</span><span class="sxs-lookup"><span data-stu-id="bb749-105">Press CTRL+N to create a new record.</span></span>

3.  <span data-ttu-id="bb749-106">في حقلي **مرحلة الخدمة** و**الوصف**، حدد معرف مرحلة الخدمة والوصف.</span><span class="sxs-lookup"><span data-stu-id="bb749-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="bb749-107">حدد المحددات المناسبة للمرحلة.</span><span class="sxs-lookup"><span data-stu-id="bb749-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="bb749-108">حدد المرحلة الأصلية للمرحلة الحالية أو اترك الحقل **الأصل** فارغًا إذا كانت المرحلة الموجودة في المرحلة الأولية في إعداد المرحلة.</span><span class="sxs-lookup"><span data-stu-id="bb749-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bb749-109">لا يمكن تعديل حقل <STRONG>الأصل</STRONG> بعد حفظ المرحلة.</span><span class="sxs-lookup"><span data-stu-id="bb749-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="bb749-110">بدلاً من ذلك، يمكنك حذف السجل وإنشاؤه مرة أخرى من خلال الاستعانة بتحديد مختلف في حقل <STRONG>الأصل</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="bb749-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="bb749-111">أيضًا، يمكن إنشاء مرحلة واحدة مع جعل حقل <STRONG>الأصل</STRONG> فارغًا.</span><span class="sxs-lookup"><span data-stu-id="bb749-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="bb749-112">وهذا يعني أنه يتم السماح ببمرحلة أولية واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="bb749-112">That is, only one initial stage is permitted.</span></span></P>


  



