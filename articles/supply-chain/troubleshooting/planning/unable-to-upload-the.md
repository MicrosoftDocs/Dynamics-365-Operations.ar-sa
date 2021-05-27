---
title: لا يمكنك تحديث تكلفة الوحدة المتوقعة عند استيراد سجلات التنبؤ بالطلب
description: عند استخدام كيانات بيانات لاستيراد سجلات التنبؤ بالطلب، لا يتم تحديث سعر التكلفة للسجلات الموجودة بحيث يتوافق مع البيانات المستوردة.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026239"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="87e9f-103">لا يمكنك تحديث تكلفة الوحدة المتوقعة عند استيراد سجلات التنبؤ بالطلب</span><span class="sxs-lookup"><span data-stu-id="87e9f-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="87e9f-104">رقم KB: 4614109</span><span class="sxs-lookup"><span data-stu-id="87e9f-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="87e9f-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="87e9f-105">Symptoms</span></span>

<span data-ttu-id="87e9f-106">عند استخدام كيانات بيانات لاستيراد سجلات التنبؤ بالطلب، لا يتم تحديث قيمة **تكلفة الوحدة المتوقعة** للسجلات الموجودة بحيث يتوافق مع البيانات المستوردة.</span><span class="sxs-lookup"><span data-stu-id="87e9f-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="87e9f-107">السبب</span><span class="sxs-lookup"><span data-stu-id="87e9f-107">Cause</span></span>

<span data-ttu-id="87e9f-108">**تكلفة الوحدة المتوقعة** عبارة عن حقل للقراءة فقط.</span><span class="sxs-lookup"><span data-stu-id="87e9f-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="87e9f-109">تعتمد القيمة على تكلفة وحدة المنتج ولا يمكن تعيينها بشكل مباشر من خلال عملية الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="87e9f-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="87e9f-110">الدقة</span><span class="sxs-lookup"><span data-stu-id="87e9f-110">Resolution</span></span>

<span data-ttu-id="87e9f-111">ونظرًاا لأن الحقل للقراءة فقط، لا يمكن استيراد القيم له.</span><span class="sxs-lookup"><span data-stu-id="87e9f-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="87e9f-112">سيتم حساب القيمة وفقًا لمنطق الأعمال الموجود.</span><span class="sxs-lookup"><span data-stu-id="87e9f-112">The value will be calculated according to the existing business logic.</span></span>
