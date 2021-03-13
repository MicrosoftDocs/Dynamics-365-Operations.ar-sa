---
title: أنواع طلبات الصيانة
description: يشرح هذا الموضوع كيفية إعداد أنواع طلبات الصيانة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56a83457097b64d195eec53000b29b2f16251772
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019319"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="3e163-103">أنواع طلبات الصيانة</span><span class="sxs-lookup"><span data-stu-id="3e163-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="3e163-104">يتم استخدام أنواع طلبات الصيانة لتصنيف طلبات الصيانة.</span><span class="sxs-lookup"><span data-stu-id="3e163-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="3e163-105">على سبيل المثال، قد يكون لديك أنواع طلبات صيانة تتعلق بالصيانة الوقائية والصيانة التصحيحية.</span><span class="sxs-lookup"><span data-stu-id="3e163-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="3e163-106">أو قد يكون لديك نوع طلب صيانة خاص يستخدم لإدارة إصلاح الأصول (إصلاح المستودع).</span><span class="sxs-lookup"><span data-stu-id="3e163-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="3e163-107">يعرّف نوع طلب الصيانة الارتباط بمجموع حالة دورة حياة طلب الصيانة (نموذج دورة حياة الصيانة).</span><span class="sxs-lookup"><span data-stu-id="3e163-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="3e163-108">تعرّف نماذج دورة حياة طلب الصيانة حالات دورة الحياة التي يمكن تعيينها لطلب صيانة.</span><span class="sxs-lookup"><span data-stu-id="3e163-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="3e163-109">(تتضمن أمثلة حالات دورة الحياة **تم الإنشاء** و **نشط** و **منتهٍ**.)</span><span class="sxs-lookup"><span data-stu-id="3e163-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="3e163-110">حدد **إدارة الأصول** \> **الإعداد** \> **طلبات الصيانة** \> **أنواع طلبات الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="3e163-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="3e163-111">حدد **جديد** لإنشاء نوع طلب صيانة.</span><span class="sxs-lookup"><span data-stu-id="3e163-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="3e163-112">في الحقل **نوع طلب الصيانة**، أدخل معرفًا لنوع طلب الصيانة.</span><span class="sxs-lookup"><span data-stu-id="3e163-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="3e163-113">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="3e163-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="3e163-114">على علامة التبويب السريعة **عام**، في حقل **نموذج دورة حياة طلب الصيانة**، حدد نموذج دورة حياة طلب صيانة.</span><span class="sxs-lookup"><span data-stu-id="3e163-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="3e163-115">في **نوع أمر العمل**، حدد نوع أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="3e163-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="3e163-116">عند تحويل طلب صيانة إلى أمر عمل، يحصل أمر العمل تلقائيًا على نوع أمر العمل المرتبط بنوع طلب الصيانة.</span><span class="sxs-lookup"><span data-stu-id="3e163-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="3e163-117">يبين الرسم التوضيحي التالي مثالاً لصفحة قائمة **أنواع طلبات الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="3e163-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![صفحة أنواع طلبات الصيانة](media/07-setup-for-requests.png)
